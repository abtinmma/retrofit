# retrofit
retrofit in life sycle and live data
# youre change aoi in retro fit in class 
class Blog👇
interface Blog {
    @GET("/{json file in url} for example comments")
    suspend fun getComments():List<comments_model>
}

class 👇 
private const val BASE_URL="https://jsonplaceholder.typicode.com/"
class Retrofiltinterface {
    private val client =OkHttpClient.Builder()
        .addInterceptor(Hederinterceptor())
        .build()
    private val moshi=Moshi.Builder()
        .add(Date::class.java,Rfc3339DateJsonAdapter())
        .addLast(KotlinJsonAdapterFactory())
        .build()
    private val retrofit by lazy {
        Retrofit.Builder()
            .baseUrl(BASE_URL)
            .client(client)
            .addConverterFactory(MoshiConverterFactory.create(moshi))
            .build()
    }
    val api:Blog by lazy {
        retrofit.create(Blog::class.java)
    }
}

folder api 
👆👆❗❗

end for retro fit in api 
