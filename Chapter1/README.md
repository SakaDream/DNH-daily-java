Như đã hứa trong topic [Dự định viết tutorial về java](https://daynhauhoc.com/t/du-dinh-viet-tutorial-ve-java/65262), hôm nay ngày 3/5/2018 mình xin ra lò series Daily Java.

# Chapter 1. Getting Started with Java

Ở đây chúng ta thảo luận về những thứ liên quan đến Java:

1. Download Java
1. Cách tải java
1. Thiết lập biến môi trường
1. Viết chương trình Java đầu tiên
1. Cách biên dịch chương trình Java
1. Cách khởi động chương trình Java


## Cách tải Java
Phiên bản JDK 8: [Java Website](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)


## Cài đặt java

- **Trên Windows**: Bạn tải java từ link trên rồi chạy file .exe bạn vừa tải. Lúc chạy được cái installer rồi thì cứ next là xong :slight_smile:

- **Trên Mac**: Sử dụng homebrew để cài đặt:

```
brew update
brew cask install java
brew tap caskroom/versions
brew cask install java8
```

- **Trên Ubuntu**: Mở terminal lên, rồi gõ các lệnh sau:

```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

Thay số 8 thành 9, 7, 6, 5,... nếu bạn muốn dùng phiên bản khác nhưng mình khuyên dùng java 8 vì nó ổn định và ít bị lỗi.

Các bước cài đặt đó chỉ chạy được trên Ubuntu, Debian, Zorin,... Chứ các distro khác thì các bạn hỏi mình mình sẽ trả lời sau!

- Sau khi cài đặt java xong thì gõ câu lệnh sau:

```
java -version
```

nếu ra dòng dưới thì tức là bạn đã cài Java thành công:

```
java version "1.8.0_51"
Java(TM) SE  Runtime  Environment (build 1.8.0_51-b16)
Java  HotSpot(TM) Client  VM (build 25.51-b03, mixed mode, sharing)
```

## Viết chương trình Java đầu tiên

Chắc hẳn câu nói vỡ lòng của bao lập trình viên là: "Hello World" nhỉ :joy:. Giờ thì chúng ta sẽ viết 1 chương trình in: "Hello DNH!"

Sử dụng trình soạn thảo bất kỳ và viết code ở phía dưới:

```java
public class FirstProgram {
	public static void main(String args[]) {
		System.out.println("Hello DNH");
	}
}
```

Lưu file với tên là ***FirstProgram.java***. Lưu ý rằng tên file phải giống như tên class trong chương trình chúng ta vừa viết. Sau khi save xong, mở terminal(hoặc cmd nếu xài windows) và chuyển tới chỗ mà bạn lưu file vừa nãy. Viết `javac FirstProgram.java` để biên dịch code java:

```
javac FirstProgram.java
```

Nếu file `.java` được biên dịch thành công thì nó sẽ tạo ra file .class ở cùng directory.

## Chạy chương trình java

Bây giờ thì chương trình java được biên dịch và chúng ta có thể chạy bằng lệnh "java" như sau:

```
java FirstProgram
Hello DNH

```

> **Note**: lệnh "java" sử dụng file .class nhưng chỉ cần điền tên thôi không cần đuôi mở rộng .class

Vậy là chúng ta đã tạo và chạy được chương trình java đầu tiên.
