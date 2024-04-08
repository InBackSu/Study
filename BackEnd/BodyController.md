## Body로 보내는 방법
1. 
```kotlin
@Controller
class HelloController {
    @GetMapping("/hello")
    fun helloMethod(): ResponseEntity<String>{
        return ResponseEntity("Hello World", HttpStatus.OK)
    }
}
```
2.
```kotlin
@Controller
class HelloController2 {
    @ResponseBody
    @GetMapping("/hello/v2")
    fun helloMethod(): String{
        return "Hello World"
    }
}
```
3.
```kotlin
@ResponseBody
@Controller
class HelloController3 {
    @GetMapping("/hello/v3")
    fun helloMethod(): String{
        return "Hello World"
    }
}
```
4.
```kotlin
@RestController
class HelloController4 {
    @GetMapping("/hello/v4")
    fun helloMethod(): String{
        return "Hello World"
    }
}
```