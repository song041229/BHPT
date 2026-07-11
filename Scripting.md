## Scripting
- 작업 자동화, 제어, 확장을 위해 작성하는 비교적 짧고 간단한 명령어 세트(스크립트)
- `shebang`
  - 어떤 인터프리터를 사용할 지 스크립터한테 알려주는 명령어
  - `#!/<인터프리터 위치>`
  - ex) `#1/bin/bash`, `#!/~~~/bin/python`

- `변수`
  - `=`저장
  - `$`사용
  ex) ipaddress=127.0.0.1
      echo "My ip address is : $ipaddress"
      출력: My ip address is : 127.0.0.1


- `if`
  - 형식
    ```
    if [<조건>]; then
      실행 명령어
    else
      실행 명령어
    fi
    ```
  
  - 조건문
    - `-ge` ">=" (greater than)의 의미
    - `-lt` "<=" (less than)의 의미
   
  - 실행하기
    1) vim에서 <파일명> 생성
    2) 내용 작성후 저장 및 종료 `wq`
    3) `chmod +x <파일명>` 실행권한 부여
    4) `$./<파일명>`으로 실행
   
  
  ex)
    <age> 파일
    ```
    age=18
    if [$age -ge 18]; then
      echo "You are an adult."
    else
      echo "You are a minor."
    fi
    ```

    $./age
    You are an adult.




- `for` 반복문
  - 형식
    ```
    for <변수명> in {n..m}
    do
      실행 명령어
    done
    ```

    ex)
      <loop> 파일
      #!/bin/bash
 
      for number in {1..5}
      do
        echo "Number: $number"
      done

      $./loop
      Number: 1
      Number: 2
      Number: 3
      Number: 4
      Number: 5
