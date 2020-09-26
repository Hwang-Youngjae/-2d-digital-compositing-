What is colorspace?
=====================
색 공간(色空間, color space)은 색 표시계(color system)를 3차원으로 표현한 공간 개념이다. 색 표시계의 모든 색들은 이 색 공간에서 3차원 좌표로 나타낸다.

여기서 색 표시계(color system)란 CIERGB, CIEXYZ, CIELAB, CIELUV 등의 색 체계를 말한다. 최근 디자인 학계나 산업계에서 색채 디자인 또는 시각 디자인을 연구하거나, 카메라, 스캐너, 모니터, 컬러 프린터 등의 컬러 영상 장비 개발 및 응용 단계에서 색 공간은 정확한 색을 재현하기 위하여 필수적으로 활용되고 있다.

특히, 색 디자인이나 디지털 색 처리에 기본적으로 사용되고 있는 색 공간인 CIELAB 색 공간은 먼셀 색 표시계의 기본 원리인 색의 3속성(색상, 명도, 채도)을 살림과 동시에 CIEXYZ 색 표시계의 불균등한 색 공간을 개선하기 위하여 개발된 것이다. 이 색 공간은 색상(hue), 명도(lightness), 채도(chroma)를 3차원 공간의 각각의 기본 축으로 하는 공간이다. 여기서 CIELAB은 CIE 1976 L*a*b*의 약식 명칭이고, CIE 1976 L*a*b*은 공식 명칭이다.

자주 쓰이는 색공간
------------------
RGB 색 공간
-----------
RGB 색 공간은 색을 혼합하면 명도가 올라가는 가산 혼합 방식으로 색을 표현한다. RGB 가산혼합의 삼원색은 빨강(Red), 녹색(Green)[1], 파랑(Blue)을 뜻한다. RGBA은 RGB와 동일하며, 알파(Alpha)라는 투과도를 덧붙인 것이다. RGB 색 공간은 삼원색에 해당하는 세 가지 채널의 밝기를 기준으로 색을 지정한다. RGB 색 공간은 웹 색상 표현의 기본 원리이다.

![200px-RGBCube_b svg](https://user-images.githubusercontent.com/71237760/94346104-67e9bb00-0065-11eb-89e5-e2781d7a9ec6.png)

CMYK 색 공간
------------
CMYK 색 공간은 인쇄과정에서 쓰이는 감산 혼합 방식으로, 흰 바탕에 네 가지 잉크의 조합으로 색을 나타내는 것을 말한다. 색을 혼합하면 명도가 낮아지기에 감산 혼합이라고 한다. CMYK는 인쇄에 쓰이는 4가지 색은 옥색(Cyan), 자홍색(Magenta), 노랑(Yellow), 검정(Black)을 뜻한다.

![200px-Synthese- svg](https://user-images.githubusercontent.com/71237760/94346119-8780e380-0065-11eb-86be-fc8dc85c8400.png)

HSV 색 공간
---------------
HSV 색 공간은 색상(Hue), 채도(Saturation), 명도(value)를 기준으로 색을 구성하는 방식이다. 감산 혼합이나 가산 혼합보다 색상의 지정이 직관적[2]이기 때문에 시각 예술에서 자주 쓰인다.

![200px-HSV_cone](https://user-images.githubusercontent.com/71237760/94346144-ae3f1a00-0065-11eb-931e-5619bd1c7d7c.jpg)

CIE 색 공간
--------------
CIE는 국제 조명 위원회(프랑스어: Commission internationale de l'éclairage)를 프랑스어식으로 표기한 준말이며, CIE 색 공간이란 컬러 매칭 실험을 통하여 생성된 R, G, B 데이터를 바탕으로 만들어진 CIEXYZ 색 공간과 CIELAB 색 공간, 그리고 CIELUV 색 공간이 대표적인 색 공간이다.

여기서 CIEXYZ 색 공간은 '균등 색 공간'이 아니어서, 이를 수식적으로 변환하여 만들어진 것이 CIELAB 색 공간과 CIELUV 색 공간이며, 이 두 색 공간은 색차를 계산할 때 비교적 정확한 계산이 이루어진다.

여기서 '균등 색 공간'이란 '불균등 색 공간'의 대립 개념이며, 불균등 공간에서는 색상들을 나타내는 선, 채도들을 나타내는 선들이 일정하지 않고 불규칙하게 배열되기 때문에 색 공간에서 두 점의 거리 즉, 색의 차이를 계산하면 정확하지 않다.
![Which-Color-Space-to-Use-When-1068x500](https://user-images.githubusercontent.com/71237760/94346160-c44cda80-0065-11eb-89e7-8d7ab03f0f53.jpeg)
출처:Wikipedia

Gamma / Linear workflow
==========================
실제 세상의 빛은 linear로 작용, 우리가 보는 빛의 양은 광원들의 빛의 양을 합친 값이다. 즉, 실제 세상에서는 input이 output과 일정, 동등하다. 이를 linear라고 한다.

![img](https://user-images.githubusercontent.com/71237760/94346335-f3b01700-0066-11eb-9edb-6fb8812cc8eb.jpg)

하지만 모니터에서는 이와 다르게 아래 그래프처럼 표시한다.

모니터가 이미지를 표현하기 위해서는 전압이 공급(input)되고, 모니터는 이를 빛의 정도로 환산해서 이미지(output)로 표현한다. 하지만 컴퓨터 모니터는 우리의 눈이 받아들일 수 있는 빛의 양을 표현할 방법이 없기 때문에 컴퓨터는 눈에 보이는 것과 유사하게 표시한다. 이를 color space라고 부른다.

![img (2)](https://user-images.githubusercontent.com/71237760/94346397-65886080-0067-11eb-8ab9-6bb9aa2a531d.jpg)

모니터들이 가장 많이 사용하는 color space는 sRGB(non-linear, 8bit, gamma 2.2) 안에서 이뤄진다. sRGB안에서는 gamma correction이라는 것이 작용하는데, 이는 우리가 본 luminance값을 비디오나 사진에서 암호화, 해독하던 방식을 말한다.

그래서 이를 다시 linear로 바로잡기 위해 의도적으로 수치값을 대입한다. 이 수치를 gamma라고 한다.

 ![img (1)](https://user-images.githubusercontent.com/71237760/94346421-7fc23e80-0067-11eb-9144-cc35973a3460.jpg)
출처:https://frauniemand.tistory.com/8

What is LUT? Color LookUpTable ?
==================================
순람표(順覽表) 또는 룩업 테이블(lookup table)은 컴퓨터 과학에서 일반적으로 배열이나 연관 배열로 된 데이터 구조로, 런타임 계산을 더 단순한 배열 색인화 과정으로 대체하는 데 자주 쓰인다. 처리 시간의 절약은 중요할 수 있는데, 이는 메모리로부터 값을 받아오는 것이 더 일이 많이 드는 계산이나 입출력 기능을 거치는 것보다 더 빠르기 때문이다.[1] 테이블들은 정적인 프로그램 저장소에 미리 계산되어 저장하거나, 프로그램 초기화 단계(메모이제이션)의 일부로 계산(프리페치)할 수도 있다. 룩업 테이블은 배열에 위치한 일련의 (올바르거나 올바르지 않은) 값 항목들을 일치시키면서 입력값이 유효한지 확인하는 데 널리 쓰이기도 하며, 프로그래밍 언어에서는 포인터 함수를 포함(또는 레이블로 오프셋)하여 일치하는 입력을 처리할 수 있다.

![How-ColorLUTs-work-in-8-bits-channel-color-spaces-a-concept-difference-between-a-1D](https://user-images.githubusercontent.com/71237760/94346510-09720c00-0068-11eb-9c6a-1e3a4481e645.png)

What is Logspace and what is main difference with sRGB, why and when we use?
===============================================================================
로그 색상 곡선을 사용하는 가장 큰 이유는 카메라 센서(또는 필름 음수)에서 가장 동적 범위의 정보를 유지하는 방법이다. 카메라가 대수적으로 보는 것을인코딩하여 이미지노출(정지 시 측정)과 녹화된 이미지 사이의 상관 관계가 더 넓은 범위에서 완전히 일정하다는것을 알수있다. 인간의 눈이나 비디오 화면을 위해 특별히 캡처하는 대신 가능한 한 많은 데이터를 저장하기 때문에 표준 비디오 곡선보다 센서의 정보를 더 많이 활용한다. 이렇게 하면 포스트 프로덕션에서 작업할 수 있는 훨씬 더 많은 색상 데이터가 제공된다.

![Log-Curve](https://user-images.githubusercontent.com/71237760/94347137-c0708680-006c-11eb-9ed8-3fcb5e769cb1.jpg)
