## Go사용해보기

* Go를 사용해 가장 쉬운 방법은 play.golang.org 라는 웹 서비스를 이용하는 방법

1. 브라우저에서 play.golang.org에 접속한다.
2. 에디터를 비우고 코드를 작성한다
~~~~~~
package main
import "fmt"

func main() {
        fmt.Println("Hello,Go!")
      }
~~~~~~
3. Froamt 버튼을 누르면 Go의 컨벤션에 따라 코드가 자동으로 정렬된다
4. Run버튼을 누른다.

-------------------------------

* 모든 Go 파일은 package절로 시작합니다. 패키지(package)란 문자열 서식 기능 모음이나 이미지 그리기 기능 모음과 같은 유사한 기능을 수행하는 코드들의 모음입니다.
* 위 코드에서는 특수 패키지인 main 패키지를 사용하는데 이 패키지는 코드를 직접 실행하는 경우에 반드시 필요한 패키지입니다.
* 대부분의 Go파일은 하나 이상의 import문을 가집니다.
* 어떤 코드에서 다른 패키지에 있는 코드를 사용하기 위해서는 먼저 해당 패키지를 가져와야(import)합니다.
* 모든 Go 코드를 한 번에 가져오게 되면 프로그램이 불필요하게 커지고 느려지기 떄문에 필요한 패키지만 가져와야 합니다.
* 이외의 나머지 부분은 실제로 실행되는 코드이며 보통은 하나 이상의 함수로 이루어져 있습니다.
* 함수(function)란 코드의 어딘가에서 호출(call)할 수 있는 한 줄 이상의 코드로 이루어진 코드의 집합입니다.
* Go 프로그램은 실행될 떄 main 함수를 가장 먼저 호출합니다.

### Go파일의 기본 형식  
대부분의 Go파일은 아래와 같이 세 부분으로 구성되어 있다.
1. package절
2. import문
3. 실제 코드

### 다른 패키지의 함수 사용하기
~~~~~~
package main

import(
        "math"
        "string"
)
func main() {
              fmt.Println(math.Floor(2.75)) //math 패키지의 Floor 함수 호출
              fmt.Println(strings.Title("head first go"))  //strings 패키지의 title함수를 호출
          }
~~~~~~
