Первый макет:
В этом макете мы используем расположение эллементов в столбик с помощью Column.  В нём мы расставляем контейнеры и пробелы(спейсеры).
Прописываем в контейнерах расположение элементов  (Margin), добавляем где нужно кнопки(ElevatedButton), настраиваем цвета и в конце добавляем картинку сидящего челика


 Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: const Color.fromARGB(255, 3, 157, 162),
      body: Column(
        crossAxisAlignment: CrossAxisAlignment.stretch,
        children: [
          Spacer(),
          Text("medinow",
              textAlign: TextAlign.center,
              style: TextStyle(
                  fontSize: 40,
                  fontWeight: FontWeight.w400,
                  color: Colors.white)),
          Text("Meditate With Us!",
              textAlign: TextAlign.center,
              style: TextStyle(
                  fontSize: 15,
                  fontWeight: FontWeight.w400,
                  color: Colors.white)),
          Spacer(),
          Container(
            height: 50,
            margin: const EdgeInsets.only(top: 12.0, left: 24, right: 24),
            child: ElevatedButton(
              onPressed: () {},
              child: Text("Sign in with Apple"),
              style: ButtonStyle(
                shape: MaterialStateProperty.all<RoundedRectangleBorder>(
                  RoundedRectangleBorder(
                    borderRadius: BorderRadius.circular(18.0),
                  ),
                ),
                backgroundColor: MaterialStateProperty.all(Colors.white),
                foregroundColor:
                    MaterialStateProperty.all(Color.fromRGBO(0, 0, 0, 1)),
              ),
            ),
          ),
          Container(
            height: 50,
            margin: const EdgeInsets.only(top: 12.0, left: 24, right: 24),
            child: ElevatedButton(
              onPressed: () {},
              child: Text("Continue with Email or Phone"),
              style: ButtonStyle(
                shape: MaterialStateProperty.all<RoundedRectangleBorder>(
                  RoundedRectangleBorder(
                    borderRadius: BorderRadius.circular(18.0),
                  ),
                ),
                backgroundColor:
                    MaterialStateProperty.all(Color.fromRGBO(205, 253, 254, 1)),
                foregroundColor:
                    MaterialStateProperty.all(Color.fromRGBO(0, 0, 0, 1)),
              ),
            ),
          ),
          Container(
            margin: const EdgeInsets.only(top: 8),
            child: const Text("Continue With Google",
                textAlign: TextAlign.center,
                style: TextStyle(
                    fontSize: 15,
                    fontWeight: FontWeight.w400,
                    color: Colors.white)),
          ),
          Spacer(),
          Container(child: Image.asset('assets/image3.png'))
        ],
      ),
    );
  }





2 Макет:

Здесь мы создаём по центру экрана контейнеры с помощью Stack ( потому что перешёл на верстку web вместо эмулятора ). Добавляем картинку и меняем её положение с помощью Margin
Далее делаем ещё контейнеры с разным текстом, который мы изменяем с помощью TextStyle и задаём каждому своё положение(Margin)
Так же добавляем на вёрстку картинки, заранее загруженные в проект, меняем им положение.

Widget build(BuildContext context) {
    return Scaffold(
        body: Center(
            child: Column(children: [
      Stack(children: [
        Container(
            child: Image.asset('assets/man.jpg'),
            margin: EdgeInsets.fromLTRB(30, 50, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(30, 300, 0, 0),
          child: Text(
            'Peter Mach',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 12,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(33, 320, 0, 0),
          child: Text(
            'Mind Deep Relax',
            style: TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 20,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(33, 350, 28, 0),
          child: Text(
            'Join the Community as we prepare over 33',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 15,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(33, 370, 28, 0),
          child: Text(
            'days to relax and feel joy with the mind',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 15,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(33, 390, 28, 0),
          child: Text(
            'and happnies session across the World.',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 15,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
            width: 342,
            margin: EdgeInsets.fromLTRB(24, 430, 0, 0),
            child: ElevatedButton(
                onPressed: () => {},
                style: ElevatedButton.styleFrom(
                    primary: Color.fromRGBO(3, 158, 162, 1),
                    padding: const EdgeInsets.all(20),
                    shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(50))),
                child: const Text(
                  ' Play Next Session',
                  textDirection: TextDirection.ltr,
                  style: TextStyle(
                    fontSize: 16,
                    fontWeight: FontWeight.normal,
                    fontStyle: FontStyle.normal,
                    color: Colors.white,
                  ),
                ))),
        Container(
          child: Image.asset(
            'Assets/he.jpg',
          ),
          margin: EdgeInsets.fromLTRB(110, 443, 0, 0),
        ),
        Container(
          child: Image.asset('assets/blue.jpg'),
          margin: EdgeInsets.fromLTRB(23, 500, 0, 0),
        ),
        Container(
          child: Text(
            'Sweet Memories',
            style: TextStyle(
              fontWeight: FontWeight.bold,
              fontSize: 17,
            ),
          ),
          margin: EdgeInsets.fromLTRB(78, 500, 0, 0),
        ),
        Container(
          child: Text(
            'December 29 Pre-Launch',
            style: TextStyle(
              fontWeight: FontWeight.normal,
              fontSize: 12,
            ),
          ),
          margin: EdgeInsets.fromLTRB(78, 520, 0, 0),
        ),
        Container(
          child: Image.asset('Assets/shape.jpg'),
          margin: EdgeInsets.fromLTRB(327, 518, 0, 0),
        ),
        Container(
          child: Image.asset('assets/pink.jpg'),
          margin: EdgeInsets.fromLTRB(23, 550, 0, 0),
        ),
        Container(
          child: Text(
            'A Day Dream',
            style: TextStyle(
              fontWeight: FontWeight.bold,
              fontSize: 17,
            ),
          ),
          margin: EdgeInsets.fromLTRB(78, 550, 0, 0),
        ),
        Container(
          child: Text(
            'December 29 Pre-Launch',
            style: TextStyle(
              fontWeight: FontWeight.normal,
              fontSize: 12,
            ),
          ),
          margin: EdgeInsets.fromLTRB(78, 575, 0, 0),
        ),
        Container(
          child: Image.asset('Assets/shape.jpg'),
          margin: EdgeInsets.fromLTRB(327, 560, 0, 0),
        ),
        Container(
          child: Image.asset('assets/hehe.jpg'),
          margin: EdgeInsets.fromLTRB(23, 600, 0, 0),
        ),
        Container(
          child: Text(
            'Mind Explore',
            style: TextStyle(
              fontWeight: FontWeight.bold,
              fontSize: 17,
            ),
          ),
          margin: EdgeInsets.fromLTRB(78, 600, 0, 0),
        ),
        Container(
          child: Text(
            'December 29 Pre-Launch',
            style: TextStyle(
              fontWeight: FontWeight.normal,
              fontSize: 12,
            ),
          ),
          margin: EdgeInsets.fromLTRB(78, 625, 0, 0),
        ),
        Container(
          child: Image.asset('Assets/shape.jpg'),
          margin: EdgeInsets.fromLTRB(327, 610, 0, 0),
        ),
      ])
    ])));
  }


3 макет:

Так же как и во втором макете создаём контейнеры по центру. Добалвяем тексты и картинки
Меняем цвета, TextStyle, и расположения.
Можно было сократить код с помощью создания одного макета и изменяя его. ( но я об этом поздно узнал :(    )



Widget build(BuildContext context) {
    return Scaffold(
        body: Center(
            child: Column(children: [
      Stack(children: [
        Container(
          margin: EdgeInsets.fromLTRB(33, 10, 0, 0),
          child: Text(
            'Meditate',
            style: TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 20,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          child: Image.asset(
            'Assets/loop.png',
          ),
          margin: EdgeInsets.fromLTRB(370, 5, 0, 0),
        ),
        Container(
            width: 52,
            margin: EdgeInsets.fromLTRB(33, 50, 0, 0),
            child: ElevatedButton(
                onPressed: () => {},
                style: ElevatedButton.styleFrom(
                    primary: Colors.blue,
                    padding: const EdgeInsets.all(20),
                    shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(50))),
                child: const Text(
                  'All',
                  textDirection: TextDirection.ltr,
                  style: TextStyle(
                    fontSize: 10,
                    fontWeight: FontWeight.normal,
                    fontStyle: FontStyle.normal,
                    color: Colors.white,
                  ),
                ))),
        Container(
            width: 103,
            margin: EdgeInsets.fromLTRB(90, 50, 0, 0),
            child: ElevatedButton(
                onPressed: () => {},
                style: ElevatedButton.styleFrom(
                    primary: Color.fromRGBO(120, 200, 239, 1),
                    padding: const EdgeInsets.all(20),
                    shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(50))),
                child: const Text(
                  'Bible In a Year',
                  textDirection: TextDirection.ltr,
                  style: TextStyle(
                    fontSize: 10,
                    fontWeight: FontWeight.normal,
                    fontStyle: FontStyle.normal,
                    color: Colors.blue,
                  ),
                ))),
        Container(
            width: 70,
            margin: EdgeInsets.fromLTRB(200, 50, 0, 0),
            child: ElevatedButton(
                onPressed: () => {},
                style: ElevatedButton.styleFrom(
                    primary: Color.fromRGBO(120, 200, 239, 1),
                    padding: const EdgeInsets.all(20),
                    shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(50))),
                child: const Text(
                  'Dailies',
                  textDirection: TextDirection.ltr,
                  style: TextStyle(
                    fontSize: 10,
                    fontWeight: FontWeight.normal,
                    fontStyle: FontStyle.normal,
                    color: Colors.blue,
                  ),
                ))),
        Container(
            width: 76,
            margin: EdgeInsets.fromLTRB(275, 50, 0, 0),
            child: ElevatedButton(
                onPressed: () => {},
                style: ElevatedButton.styleFrom(
                    primary: Color.fromRGBO(120, 200, 239, 1),
                    padding: const EdgeInsets.all(20),
                    shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(50))),
                child: const Text(
                  'Minutes',
                  textDirection: TextDirection.ltr,
                  style: TextStyle(
                    fontSize: 10,
                    fontWeight: FontWeight.normal,
                    fontStyle: FontStyle.normal,
                    color: Colors.blue,
                  ),
                ))),
        Container(
            width: 70,
            margin: EdgeInsets.fromLTRB(360, 50, 0, 0),
            child: ElevatedButton(
                onPressed: () => {},
                style: ElevatedButton.styleFrom(
                    primary: Color.fromRGBO(120, 200, 239, 1),
                    padding: const EdgeInsets.all(20),
                    shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(50))),
                child: const Text(
                  'Noven',
                  textDirection: TextDirection.ltr,
                  style: TextStyle(
                    fontSize: 10,
                    fontWeight: FontWeight.normal,
                    fontStyle: FontStyle.normal,
                    color: Colors.blue,
                  ),
                ))),
        Container(
            child: Image.asset(
              'Assets/moon.png',
            ),
            margin: EdgeInsets.fromLTRB(33, 100, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(33, 340, 0, 0),
          child: Text(
            'A Song of Moon',
            style: TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 20,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(33, 365, 0, 0),
          child: Text(
            'Start with the basics',
            style: TextStyle(fontSize: 14, fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
            child: Image.asset(
              'Assets/heart.png',
            ),
            margin: EdgeInsets.fromLTRB(33, 385, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(50, 385, 0, 0),
          child: Text(
            '9 Sessions',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(365, 385, 0, 0),
          child: Text(
            'Start',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(397, 382, 0, 0),
          child: Text(
            '>',
            style: TextStyle(fontSize: 18, fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
            child: Image.asset(
              'Assets/Sky2.png',
            ),
            margin: EdgeInsets.fromLTRB(33, 420, 0, 0)),

        Container(
          margin: EdgeInsets.fromLTRB(33, 525, 0, 0),
          child: Text(
            'The Sleep Hour',
            style: TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 20,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(33, 550, 0, 0),
          child: Text(
            'Ashna Mukherjree',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
            child: Image.asset(
              'Assets/heart.png',
            ),
            margin: EdgeInsets.fromLTRB(33, 575, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(50, 575, 0, 0),
          child: Text(
            '3 Sessions',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(153, 575, 0, 0),
          child: Text(
            'Start',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(185, 571, 0, 0),
          child: Text(
            '>',
            style: TextStyle(fontSize: 18, fontFamily: 'PlusJakartaSans'),
          ),
        ),

        ///
        ///
        ///
        ///
        ///
        Container(
            child: Image.asset(
              'Assets/Sky3.png',
            ),
            margin: EdgeInsets.fromLTRB(260, 420, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(260, 525, 0, 0),
          child: Text(
            'Easy on the Mission',
            style: TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 18,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),

        Container(
          margin: EdgeInsets.fromLTRB(260, 550, 0, 0),
          child: Text(
            'Peter Mach',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
            child: Image.asset(
              'Assets/heart.png',
            ),
            margin: EdgeInsets.fromLTRB(260, 575, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(277, 575, 0, 0),
          child: Text(
            '5 minutes',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(370, 575, 0, 0),
          child: Text(
            'Start',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(402, 572, 0, 0),
          child: Text(
            '>',
            style: TextStyle(fontSize: 18, fontFamily: 'PlusJakartaSans'),
          ),
        ),
        //

        //

        ///
        ///
        /////
        ///
        ///
        ///
        ///
        ///
        ///
        Container(
            child: Image.asset(
              'Assets/Sky4.png',
            ),
            margin: EdgeInsets.fromLTRB(33, 610, 0, 0)),

        Container(
          margin: EdgeInsets.fromLTRB(33, 715, 0, 0),
          child: Text(
            'Relax with me',
            style: TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 20,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(33, 740, 0, 0),
          child: Text(
            'Amanda James',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
            child: Image.asset(
              'Assets/heart.png',
            ),
            margin: EdgeInsets.fromLTRB(33, 770, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(50, 770, 0, 0),
          child: Text(
            '3 Sessions',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(153, 770, 0, 0),
          child: Text(
            'Start',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(185, 768, 0, 0),
          child: Text(
            '>',
            style: TextStyle(fontSize: 18, fontFamily: 'PlusJakartaSans'),
          ),
        ),

        ///
        ///
        ///
        ///
        ///
        Container(
            child: Image.asset(
              'Assets/Sky5.png',
            ),
            margin: EdgeInsets.fromLTRB(260, 610, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(260, 715, 0, 0),
          child: Text(
            'Sun and Energy',
            style: TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 20,
                fontFamily: 'PlusJakartaSans'),
          ),
        ),

        Container(
          margin: EdgeInsets.fromLTRB(260, 740, 0, 0),
          child: Text(
            'Michael Hiu',
            style: TextStyle(
                fontWeight: FontWeight.normal,
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),

        Container(
            child: Image.asset(
              'Assets/heart.png',
            ),
            margin: EdgeInsets.fromLTRB(260, 770, 0, 0)),
        Container(
          margin: EdgeInsets.fromLTRB(277, 770, 0, 0),
          child: Text(
            '5 minutes',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(370, 770, 0, 0),
          child: Text(
            'Start',
            style: TextStyle(
                fontSize: 14,
                fontFamily: 'PlusJakartaSans',
                color: Colors.grey),
          ),
        ),
        Container(
          margin: EdgeInsets.fromLTRB(402, 768, 0, 0),
          child: Text(
            '>',
            style: TextStyle(fontSize: 18, fontFamily: 'PlusJakartaSans'),
          ),
        ),
      ])
    ])));
  }
