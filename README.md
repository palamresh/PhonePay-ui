# PhonePay-ui



//main file 
import 'package:awesome_icons/awesome_icons.dart';
import 'package:buttonnavigationbar/pages/fifth_page.dart';
import 'package:buttonnavigationbar/pages/first_page.dart';
import 'package:buttonnavigationbar/pages/fourth_page.dart';
import 'package:buttonnavigationbar/pages/third_page.dart';
import 'package:flutter/material.dart';


// import 'first_page/to_mobile.dart';
import 'pages/second_page.dart';

void main() {
  runApp(MaterialApp(
    // initialRoute: "/",
    // routes: {
    //   "/": (context) => ToMobile(),
    // },
    debugShowCheckedModeBanner: false,
    theme: ThemeData(primarySwatch: Colors.deepPurple),
    home: const HomePage(),
  ));
}

class HomePage extends StatefulWidget {
  const HomePage({super.key});

  @override
  State<HomePage> createState() => _HomePageState();
}

class _HomePageState extends State<HomePage> {
  var selectItem = [
    const FirstPage(),
    const SecondPage(),
    const ThirdPage(),
    const FourthPage(),
    const FifthPage()
  ];

  var _currentIndex = 0;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Row(
          children: [
            Container(
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10.0),
                color: Colors.white,
              ),
              height: 40,
              width: 40,
              child: const Icon(
                Icons.person,
                color: Colors.deepPurple,
                size: 30.0,
              ),
            ),
            const SizedBox(
              width: 6.0,
            ),
            Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              // ignore: prefer_const_literals_to_create_immutables
              children: [
                const Text(
                  "Add Address",
                  style: TextStyle(fontSize: 18.0),
                ),
                const Text(
                  'Here is your location',
                  style: TextStyle(fontSize: 14.0),
                )
              ],
            ),
            const SizedBox(width: 30),
            IconButton(
                onPressed: () {},
                icon: const Icon(
                  Icons.rounded_corner_outlined,
                  size: 33.0,
                )),
            const SizedBox(
              width: 10,
            ),
            IconButton(
                onPressed: () {},
                icon: const Icon(
                  FontAwesomeIcons.bell,
                  size: 22.0,
                )),
            IconButton(
              onPressed: () {},
              icon: const Icon(
                Icons.question_mark,
              ),
            )
          ],
        ),
      ),
      body: selectItem[_currentIndex],
      bottomNavigationBar: BottomNavigationBar(
          // backgroundColor: Colors.orange,
          selectedItemColor: Colors.deepPurple.shade900,

          // selectedFontSize: 20.0,
          selectedIconTheme: IconThemeData(color: Colors.deepPurple.shade900),
          unselectedItemColor: Colors.deepPurple.shade200,
          unselectedIconTheme: IconThemeData(color: Colors.deepPurple.shade200),
          showUnselectedLabels: true,
          type: BottomNavigationBarType.fixed,
          // ignore: prefer_const_literals_to_create_immutables
          items: [
            const BottomNavigationBarItem(
              icon: Icon(
                FontAwesomeIcons.home,
                size: 23.0,
                // color: Colors.black,
              ),
              label: "Home",
            ),
            const BottomNavigationBarItem(
                icon: Icon(
                  FontAwesomeIcons.lock,
                  size: 23.0,
                  // color: Colors.black,
                ),
                label: "Store"),
            const BottomNavigationBarItem(
                icon: Icon(
                  FontAwesomeIcons.infinity,
                  size: 23.0,
                  // color: Colors.black,
                ),
                label: "Insurance"),
            const BottomNavigationBarItem(
                icon: Icon(
                  FontAwesomeIcons.wallet,
                  size: 23.0,
                  // color: Colors.black,
                ),
                label: "Wealth"),
            const BottomNavigationBarItem(
                icon: Icon(
                  FontAwesomeIcons.database,
                  size: 23.0,
                  // color: Colors.black,
                ),
                label: "History")
          ],
          currentIndex: _currentIndex,
          onTap: (value) {
            setState(() {
              _currentIndex = value;
            });
          }),
    );
  }
}


// Firstpage
// ignore_for_file: unnecessary_string_escapes

import 'package:awesome_icons/awesome_icons.dart';
import 'package:buttonnavigationbar/first_page/to_mobile.dart';
// import 'package:buttonnavigationbar/main.dart';
import 'package:flutter/material.dart';

class FirstPage extends StatelessWidget {
  const FirstPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.deepPurple.shade100,
      body: ListView(
        physics: const BouncingScrollPhysics(),
        children: [
          Container(
            padding: const EdgeInsets.all(10.0),
            margin: const EdgeInsets.all(10.0),
            height: 150,
            width: 400,
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            child: Column(
              children: [
                Row(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: [
                    const CircleAvatar(
                      radius: 30,
                      backgroundColor: Colors.deepPurple,
                      child: Icon(
                        FontAwesomeIcons.facebook,
                        size: 40,
                        color: Colors.white,
                      ),
                    ),
                    const SizedBox(
                      width: 20,
                    ),
                    Column(
                      crossAxisAlignment: CrossAxisAlignment.start,
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        const Text(
                          'Get more with the new Update',
                          style: TextStyle(
                              fontSize: 13.0, fontWeight: FontWeight.bold),
                        ),
                        const Text(
                          "We\'ve enhanced the app, and adddedt\nsome new and exciting features",
                          style: TextStyle(fontSize: 12.0),
                        )
                      ],
                    ),
                  ],
                ),
                Row(
                  children: [
                    const SizedBox(
                      width: 110,
                    ),
                    TextButton(
                        onPressed: () {},
                        child: const Text(
                          "LATER",
                          style: TextStyle(fontSize: 16.0),
                        )),
                    const SizedBox(
                      width: 20,
                    ),
                    ElevatedButton(
                      onPressed: () {},
                      style: ElevatedButton.styleFrom(
                          shape: const StadiumBorder()),
                      child: const Text("DOWNLOAD"),
                    )
                  ],
                )
              ],
            ),
          ),
          const SizedBox(
            height: 1,
          ),
          SingleChildScrollView(
            scrollDirection: Axis.horizontal,
            child: Row(
              children: [
                Container(
                  // padding: EdgeInsets.only(right: 10, left: 10),
                  margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                  height: 150,
                  width: 370,
                  decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(10.0),
                      color: Colors.teal),
                  child: Card(
                      child: Image.asset("lib/assets/car1.jpg",
                          fit: BoxFit.cover)),
                ),
                Container(
                  // padding: EdgeInsets.only(right: 10, left: 10),
                  margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                  height: 150,
                  width: 370,
                  decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(10.0),
                      color: Colors.orange),
                  child: Card(
                    child: Image.asset(
                      "lib/assets/car2.jpg",
                      fit: BoxFit.cover,
                    ),
                  ),
                ),
                Container(
                  // padding: EdgeInsets.only(right: 10, left: 10),
                  margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                  height: 150,
                  width: 370,
                  decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(10.0),
                      color: Colors.green),
                  child: Card(
                    child: Image.asset(
                      "lib/assets/car3.jpg",
                      fit: BoxFit.cover,
                    ),
                  ),
                ),
                Container(
                  // padding: EdgeInsets.only(right: 10, left: 10),
                  margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                  height: 150,
                  width: 370,
                  decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(10.0),
                      color: Colors.cyan),
                  child: Card(
                    child: Image.asset(
                      "lib/assets/train.jpg",
                      fit: BoxFit.cover,
                    ),
                  ),
                ),
                Container(
                  // padding: EdgeInsets.only(right: 10, left: 10),
                  margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                  height: 150,
                  width: 370,
                  decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(10.0),
                      color: Colors.pink),
                  child: Card(
                      child: Image.asset("lib/assets/flight.jpg",
                          fit: BoxFit.cover)),
                )
              ],
            ),
          ),
          const SizedBox(
            height: 1,
          ),
          Container(
            margin: const EdgeInsets.all(10.0),
            height: 220,
            width: 400,
            decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10.0), color: Colors.white),
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: [
                const Center(
                  child: Text(
                    "Transfer Money",
                    textAlign: TextAlign.end,
                    style: TextStyle(
                      fontSize: 18.0,
                      fontWeight: FontWeight.bold,
                    ),
                  ),
                ),
                const SizedBox(
                  height: 23,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  children: [
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: Container(
                        height: 60,
                        width: 60,
                        decoration: BoxDecoration(
                            borderRadius: BorderRadius.circular(10.0),
                            color: Colors.deepPurple),
                        child: const Icon(
                          Icons.person,
                          size: 30,
                          color: Colors.white,
                        ),
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: Container(
                        height: 60,
                        width: 60,
                        decoration: BoxDecoration(
                            borderRadius: BorderRadius.circular(10.0),
                            color: Colors.deepPurple),
                        child: const Icon(
                          Icons.home,
                          size: 30,
                          color: Colors.white,
                        ),
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: Container(
                        height: 60,
                        width: 60,
                        decoration: BoxDecoration(
                            borderRadius: BorderRadius.circular(10.0),
                            color: Colors.deepPurple),
                        child: const Icon(
                          Icons.punch_clock_sharp,
                          size: 30,
                          color: Colors.white,
                        ),
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: Container(
                        height: 60,
                        width: 60,
                        decoration: BoxDecoration(
                            borderRadius: BorderRadius.circular(10.0),
                            color: Colors.deepPurple),
                        child: const Icon(
                          FontAwesomeIcons.home,
                          size: 30,
                          color: Colors.white,
                        ),
                      ),
                    )
                  ],
                ),
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    const Text("   To Mobile \n   Number"),
                    const SizedBox(
                      width: 4,
                    ),
                    const Text(
                      '  To Bank \n   UPI ID',
                      style: TextStyle(),
                    ),
                    const Text("       To Self\n      Account"),
                    const Text("          Check \n        Bank Balance")
                  ],
                ),
                const SizedBox(
                  height: 20,
                ),
                Container(
                  decoration: BoxDecoration(
                      color: Colors.teal.shade200,
                      borderRadius: const BorderRadius.only(
                          bottomLeft: Radius.circular(10.0),
                          bottomRight: Radius.circular(10.0))),
                  height: 53,
                  width: double.infinity,
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      // ignore: prefer_const_constructors
                      Text(
                        "    My UPI ID: 7081461044@ybl",
                        style: const TextStyle(fontWeight: FontWeight.bold),
                      ),
                      const Padding(
                        padding: EdgeInsets.only(right: 20),
                        child: Icon(
                          FontAwesomeIcons.arrowRight,
                          size: 20,
                        ),
                      )
                    ],
                  ),
                )
              ],
            ),
          ),
          Row(
            mainAxisAlignment: MainAxisAlignment.spaceAround,
            children: [
              Container(
                decoration: BoxDecoration(
                  borderRadius: BorderRadius.circular(10.0),
                  color: const Color.fromARGB(255, 33, 121, 243),
                ),
                height: 80,
                width: 115,
                child: Center(
                  child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      const Icon(
                        Icons.wallet_giftcard_outlined,
                        size: 30,
                        color: Colors.white,
                      ),
                      const Text(
                        "PhonePe Wallet",
                        style: TextStyle(color: Colors.white),
                      )
                    ],
                  ),
                ),
              ),
              Container(
                decoration: BoxDecoration(
                  borderRadius: BorderRadius.circular(10.0),
                  color: const Color.fromARGB(255, 33, 121, 243),
                ),
                height: 80,
                width: 115,
                child: Center(
                  child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      const Icon(
                        Icons.recent_actors,
                        size: 30,
                        color: Colors.white,
                      ),
                      const Text(
                        "Rewards",
                        style: TextStyle(color: Colors.white),
                      )
                    ],
                  ),
                ),
              ),
              Container(
                decoration: BoxDecoration(
                  borderRadius: BorderRadius.circular(10.0),
                  color: const Color.fromARGB(255, 33, 121, 243),
                ),
                height: 80,
                width: 115,
                child: Center(
                  child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      const Icon(
                        Icons.share,
                        size: 30,
                        color: Colors.white,
                      ),
                      const Text(
                        "Refer & Get €20",
                        style: TextStyle(color: Colors.white),
                      )
                    ],
                  ),
                ),
              ),
            ],
          ),
          const SizedBox(
            height: 10,
          ),
          Container(
            margin: const EdgeInsets.all(10.0),
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            height: 250,
            width: 300,
            child: Column(
              children: [
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceAround,
                  children: [
                    const Text(
                      'Recharge & Pay Bills',
                      style: TextStyle(fontWeight: FontWeight.bold),
                    ),
                    Container(
                      decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(40.0),
                        color: Colors.deepPurple.shade200,
                      ),
                      height: 30,
                      width: 80,
                      child: const Center(child: Text("My Bills")),
                    )
                  ],
                ),
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        Icons.electric_bolt,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        Icons.data_thresholding,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        Icons.electric_bike,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        FontAwesomeIcons.creditCard,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    )
                  ],
                ),
                const SizedBox(
                  height: 7,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    const Text("      Mobile \n     Number"),
                    const SizedBox(
                      width: 4,
                    ),
                    const Text(
                      '       DTH',
                      style: TextStyle(),
                    ),
                    const Text("             Electricity"),
                    const Text("    Credit card \n   Bill Payment")
                  ],
                ),
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  children: [
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: InkWell(
                        onTap: () {
                          Navigator.push(
                              context,
                              MaterialPageRoute(
                                  builder: (context) => const ToMobile()));
                        },
                        child: const Icon(
                          FontAwesomeIcons.houseDamage,
                          size: 40,
                          color: Colors.deepPurple,
                        ),
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        FontAwesomeIcons.wineBottle,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    const InkWell(
                      child: Icon(
                        Icons.cast_for_education_rounded,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    Container(
                      height: 50,
                      width: 50,
                      decoration: BoxDecoration(
                          borderRadius: BorderRadius.circular(10.0),
                          color: Colors.deepPurple),
                      child: const Icon(
                        Icons.arrow_back_ios_new_sharp,
                        size: 20,
                        color: Colors.white,
                      ),
                    )
                  ],
                ),
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    const Text("          Rent \n      Payment"),
                    const SizedBox(
                      width: 4,
                    ),
                    const Text(
                      '         Loan \n     RePayment',
                      style: TextStyle(),
                    ),
                    const Text("       Education\n         Fees"),
                    const Text("     See All \n                             ")
                  ],
                ),
              ],
            ),
          ),
          Container(
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            margin: const EdgeInsets.all(10.0),
            height: 150,
            width: 400,
            child: Column(
              children: [
                const Center(
                    child: Text(
                  "Sponsored  Links",
                  style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
                )),
                const SizedBox(
                  height: 10.0,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceAround,
                  children: [
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                            radius: 30,
                            backgroundImage: AssetImage("lib/assets/bujaj.jpg"),
                          ),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Bajaj Finserv",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        const InkWell(
                          child: CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage('lib/assets/rummycircle.jpg')),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "RummyCircle",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/kotak.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Kotak811",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/rummyCulture.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "RummyCul-ture",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    )
                  ],
                )
              ],
            ),
          ),
          Container(
            margin: const EdgeInsets.all(8.0),
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            height: 250,
            width: 300,
            child: Column(
              children: [
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceAround,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    const Text(
                      'Insurance',
                      style:
                          TextStyle(fontWeight: FontWeight.bold, fontSize: 20),
                    ),
                  ],
                ),
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: InkWell(
                        onTap: () {
                          Navigator.push(
                              context,
                              MaterialPageRoute(
                                  builder: (context) => const ToMobile()));
                        },
                        child: InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const InkWell(
                            child: Icon(
                              Icons.h_mobiledata,
                              size: 40,
                              color: Colors.deepPurple,
                            ),
                          ),
                        ),
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        FontAwesomeIcons.car,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        Icons.health_and_safety,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        FontAwesomeIcons.personBooth,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    )
                  ],
                ),
                const SizedBox(
                  height: 7,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    const Text("      Bike \n     "),
                    const SizedBox(
                      width: 4,
                    ),
                    const Text(
                      'Car',
                      style: TextStyle(),
                    ),
                    const Text("Health++"),
                    const Text("    Person\n Accident")
                  ],
                ),
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  children: [
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: InkWell(
                        onTap: () {
                          Navigator.push(
                              context,
                              MaterialPageRoute(
                                  builder: (context) => const ToMobile()));
                        },
                        child: InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const Icon(
                            FontAwesomeIcons.houseDamage,
                            size: 40,
                            color: Colors.deepPurple,
                          ),
                        ),
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        FontAwesomeIcons.wineBottle,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    InkWell(
                      onTap: () {
                        Navigator.push(
                            context,
                            MaterialPageRoute(
                                builder: (context) => const ToMobile()));
                      },
                      child: const Icon(
                        Icons.cast_for_education_rounded,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                    ),
                    Container(
                      height: 50,
                      width: 50,
                      decoration: BoxDecoration(
                          borderRadius: BorderRadius.circular(10.0),
                          color: Colors.deepPurple),
                      child: const Icon(
                        Icons.arrow_back_ios_new_sharp,
                        size: 20,
                        color: Colors.white,
                      ),
                    )
                  ],
                ),
                const SizedBox(
                  height: 10,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    const Text("          Rent \n      Payment"),
                    const SizedBox(
                      width: 4,
                    ),
                    const Text(
                      '         Loan \n     RePayment',
                      style: TextStyle(),
                    ),
                    const Text("       Education\n         Fees"),
                    const Text("     See All \n                             ")
                  ],
                ),
              ],
            ),
          ),
          Container(
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            margin: const EdgeInsets.all(10.0),
            height: 150,
            width: 400,
            child: Column(
              children: [
                const Center(
                    child: Text(
                  "Travel Booking",
                  style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
                )),
                const SizedBox(
                  height: 10.0,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceAround,
                  children: [
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage: AssetImage(
                                "lib/assets/flight.jpg",
                              )),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Flights",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/train.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Trains",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                            radius: 30,
                            backgroundImage: AssetImage("lib/assets/car1.jpg"),
                          ),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Car",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/hotel.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Hotels",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    )
                  ],
                )
              ],
            ),
          ),
          Container(
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            margin: const EdgeInsets.all(10.0),
            height: 150,
            width: 400,
            child: Column(
              children: [
                const Center(
                    child: Text(
                  "Switch",
                  style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
                )),
                const SizedBox(
                  height: 10.0,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceAround,
                  children: [
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/swiggy.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Swiggy",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                            radius: 30,
                            backgroundImage:
                                AssetImage("lib/assets/bugfastag.jpg"),
                          ),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "BusFastag",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        const InkWell(
                          child: CircleAvatar(
                            radius: 30,
                            backgroundImage:
                                AssetImage("lib/assets/myntra.jpg"),
                          ),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Myntra",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                            radius: 30,
                            child: Icon(
                              Icons.arrow_circle_right,
                              size: 40.0,
                            ),
                          ),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "See All",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    )
                  ],
                )
              ],
            ),
          ),
          Container(
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            margin: const EdgeInsets.all(10.0),
            height: 150,
            width: 400,
            child: Column(
              children: [
                const Center(
                    child: Text(
                  "Subscriptions",
                  style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
                )),
                const SizedBox(
                  height: 10.0,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceAround,
                  children: [
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/hotstar.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Hotstar",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/tinder.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Tinder",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/zee5.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Zee5",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                            radius: 30,
                            child: Icon(Icons.arrow_circle_right_outlined,
                                size: 40),
                          ),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "See All",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    )
                  ],
                )
              ],
            ),
          ),
          Container(
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            margin: const EdgeInsets.all(10.0),
            height: 150,
            width: 400,
            child: Column(
              children: [
                const Center(
                    child: Text(
                  "Sponsored Games",
                  style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
                )),
                const SizedBox(
                  height: 10.0,
                ),
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceAround,
                  children: [
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        const InkWell(
                          child: CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/a23.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "A23 Rummuy",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/rummytime.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "RummyTime",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: InkWell(
                            onTap: () {
                              Navigator.push(
                                  context,
                                  MaterialPageRoute(
                                      builder: (context) => const ToMobile()));
                            },
                            child: const CircleAvatar(
                                radius: 30,
                                backgroundImage:
                                    AssetImage("lib/assets/zupee.jpg")),
                          ),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Zupee",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    ),
                    Column(
                      // ignore: prefer_const_literals_to_create_immutables
                      children: [
                        InkWell(
                          onTap: () {
                            Navigator.push(
                                context,
                                MaterialPageRoute(
                                    builder: (context) => const ToMobile()));
                          },
                          child: const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/junglyrummy.jpg")),
                        ),
                        const SizedBox(
                          height: 10,
                        ),
                        const Text(
                          "Junglee Rummy",
                          style: TextStyle(fontWeight: FontWeight.bold),
                        )
                      ],
                    )
                  ],
                )
              ],
            ),
          ),
        ],
      ),
    );
  }
}
//second page

// ignore_for_file: unnecessary_string_escapes

// import 'package:awesome_icons/awesome_icons.dart';
import 'package:flutter/material.dart';

class SecondPage extends StatelessWidget {
  const SecondPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.deepPurple.shade100,
      body: Padding(
          padding: const EdgeInsets.all(8.0),
          child: ListView(
            physics: const BouncingScrollPhysics(),
            children: [
              TextField(
                decoration: InputDecoration(
                    filled: true,
                    fillColor: Colors.white,
                    border: OutlineInputBorder(
                        borderRadius: BorderRadius.circular(33.0)),
                    prefixIcon: const Icon(Icons.search_outlined),
                    hintText: "Search by store name or phone number",
                    hintStyle: const TextStyle(fontSize: 16.0)),
              ),
              const SizedBox(
                height: 9.0,
              ),
              Container(
                height: 155,
                width: 390,
                decoration: BoxDecoration(
                    color: Colors.white,
                    borderRadius: BorderRadius.circular(10.0)),
                child: Column(
                  children: [
                    const SizedBox(
                      height: 10,
                    ),
                    const Text(
                        'Last Payment form ₹9000 more than 6 months ago'),
                    const SizedBox(
                      height: 10,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                          radius: 30,
                          backgroundImage:
                              AssetImage('lib/assets/kiranastore.jpg')),
                      title: Text("Yogi Mobile"),
                      subtitle: Text("4.0  701 m  Closed at 10:00 pm"),
                      trailing: Padding(
                        padding: EdgeInsets.only(right: 10.0),
                        child: Text(
                          ">",
                          style: TextStyle(fontSize: 30.0),
                        ),
                      ),
                    ),
                    Container(
                      height: 34,
                      width: 330,
                      decoration: BoxDecoration(
                          borderRadius: BorderRadius.circular(10.0),
                          color: Colors.deepPurple.shade100),
                      child: const Center(
                        child: Text("₹  Pay Now"),
                      ),
                    ),
                  ],
                ),
              ),
              const SizedBox(
                height: 9.0,
              ),
              Container(
                height: 155,
                width: 390,
                decoration: BoxDecoration(
                    color: Colors.white,
                    borderRadius: BorderRadius.circular(10.0)),
                child: Column(
                  children: [
                    const SizedBox(
                      height: 10,
                    ),
                    const Text('Last Payment form ₹40 more than 6 months '),
                    const SizedBox(
                      height: 10,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        backgroundImage: AssetImage('lib/assets/car1.jpg'),
                      ),
                      title: Text("Veer Teza"),
                      subtitle: Text("4.0  701 m  Closed at 10:00 pm"),
                      trailing: Padding(
                        padding: EdgeInsets.only(right: 10.0),
                        child: Text(
                          ">",
                          style: TextStyle(fontSize: 30.0),
                        ),
                      ),
                    ),
                    Container(
                      height: 34,
                      width: 330,
                      decoration: BoxDecoration(
                          borderRadius: BorderRadius.circular(10.0),
                          color: Colors.deepPurple.shade100),
                      child: const Center(
                        child: Text("₹  Pay Now"),
                      ),
                    ),
                  ],
                ),
              ),
              const SizedBox(
                height: 9.0,
              ),
              Container(
                height: 155,
                width: 390,
                decoration: BoxDecoration(
                    color: Colors.white,
                    borderRadius: BorderRadius.circular(10.0)),
                child: Column(
                  children: [
                    const SizedBox(
                      height: 10,
                    ),
                    const Text('Last Payment form ₹400 more than 6 months ago'),
                    const SizedBox(
                      height: 10,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        backgroundImage: AssetImage("lib/assets/doctor.jpg"),
                      ),
                      title: Text("Tirupati Medical Store"),
                      subtitle: Text("4.0  701 m  Closed at 10:00 pm"),
                      trailing: Padding(
                        padding: EdgeInsets.only(right: 10.0),
                        child: Text(
                          ">",
                          style: TextStyle(fontSize: 30.0),
                        ),
                      ),
                    ),
                    Container(
                      height: 34,
                      width: 330,
                      decoration: BoxDecoration(
                          borderRadius: BorderRadius.circular(10.0),
                          color: Colors.deepPurple.shade100),
                      child: const Center(
                        child: Text("₹  Pay Now"),
                      ),
                    ),
                  ],
                ),
              ),
              const SizedBox(
                height: 9.0,
              ),
              Container(
                height: 155,
                width: 390,
                decoration: BoxDecoration(
                    color: Colors.white,
                    borderRadius: BorderRadius.circular(10.0)),
                child: Column(
                  children: [
                    const SizedBox(
                      height: 10,
                    ),
                    const Text('Last Payment form ₹500 more than 6 months ago'),
                    const SizedBox(
                      height: 10,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        backgroundImage: AssetImage('lib/assets/pharamacy.jpg'),
                      ),
                      title: Text("Yash Traders"),
                      subtitle: Text("4.0  701 m  Closed at 10:00 pm"),
                      trailing: Padding(
                        padding: EdgeInsets.only(right: 10.0),
                        child: Text(
                          ">",
                          style: TextStyle(fontSize: 30.0),
                        ),
                      ),
                    ),
                    Container(
                      height: 34,
                      width: 330,
                      decoration: BoxDecoration(
                          borderRadius: BorderRadius.circular(10.0),
                          color: Colors.deepPurple.shade100),
                      child: const Center(
                        child: Text("₹  Pay Now"),
                      ),
                    ),
                  ],
                ),
              ),
              const SizedBox(
                height: 9.0,
              ),
              Container(
                height: 155,
                width: 390,
                decoration: BoxDecoration(
                    color: Colors.white,
                    borderRadius: BorderRadius.circular(10.0)),
                child: Column(
                  children: [
                    const SizedBox(
                      height: 10,
                    ),
                    const Text('Last Payment form ₹200 more than 6 months ago'),
                    const SizedBox(
                      height: 10,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        backgroundImage:
                            AssetImage("lib/assets/stationary.jpg"),
                      ),
                      title: Text("Text Book"),
                      subtitle: Text("4.0  701 m  Closed at 10:00 pm"),
                      trailing: Padding(
                        padding: EdgeInsets.only(right: 10.0),
                        child: Text(
                          ">",
                          style: TextStyle(fontSize: 30.0),
                        ),
                      ),
                    ),
                    Container(
                      height: 34,
                      width: 330,
                      decoration: BoxDecoration(
                          borderRadius: BorderRadius.circular(10.0),
                          color: Colors.deepPurple.shade100),
                      child: const Center(
                        child: Text("₹  Pay Now"),
                      ),
                    ),
                  ],
                ),
              ),
              const SizedBox(
                height: 9.0,
              ),
              Container(
                height: 350,
                width: 390,
                decoration: BoxDecoration(
                    color: Colors.white,
                    borderRadius: BorderRadius.circular(10.0)),
                child: Column(
                  children: [
                    const SizedBox(
                      height: 9.0,
                    ),
                    const Text("Popular Categories"),
                    const SizedBox(
                      height: 10.0,
                    ),
                    Row(
                      mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                      children: [
                        Column(
                          children: const [
                            CircleAvatar(
                                radius: 30,
                                backgroundImage:
                                    AssetImage("lib/assets/kiranastore.jpg")),
                            SizedBox(
                              height: 5.0,
                            ),
                            Text(
                              "     Kirana & \nGeneral Stores",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                                radius: 30,
                                backgroundImage:
                                    AssetImage("lib/assets/fruits.jpg")),
                            const SizedBox(
                              height: 5.0,
                            ),
                            const Text(
                              "Fruits and \nVegetables",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/meetshops.jpg"),
                            ),
                            const SizedBox(
                              height: 9.0,
                            ),
                            const Text(
                              "Meat & \Shops",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/pharamacy.jpg"),
                            ),
                            const SizedBox(
                              height: 9.0,
                            ),
                            const Text(
                              "Pharamacy ",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                      ],
                    ),
                    const SizedBox(
                      height: 10.0,
                    ),
                    Row(
                      mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                      children: [
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/doctor.jpg"),
                            ),
                            const SizedBox(
                              height: 5.0,
                            ),
                            const Text(
                              " Doctore & \npath labs",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/food.jpg"),
                            ),
                            const SizedBox(
                              height: 5.0,
                            ),
                            const Text(
                              "   Food & \nBeberages",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                                radius: 30,
                                backgroundImage:
                                    AssetImage("lib/assets/salon.jpg")),
                            const SizedBox(
                              height: 9.0,
                            ),
                            const Text(
                              "Salon & \nSpa",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                                radius: 30,
                                backgroundImage:
                                    AssetImage("lib/assets/home.jpg")),
                            const SizedBox(
                              height: 9.0,
                            ),
                            const Text(
                              "Home repain \nand cleaning ",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                      ],
                    ),
                    const SizedBox(
                      height: 10.0,
                    ),
                    Row(
                      mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                      children: [
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                                radius: 30,
                                backgroundImage:
                                    AssetImage("lib/assets/stationary.jpg")),
                            const SizedBox(
                              height: 5.0,
                            ),
                            const Text(
                              "     Stationary ",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                              radius: 30,
                              backgroundImage: AssetImage("lib/assets/pet.jpg"),
                            ),
                            const SizedBox(
                              height: 5.0,
                            ),
                            const Text(
                              "Pet shop",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                              radius: 30,
                              backgroundImage:
                                  AssetImage("lib/assets/toyshops.jpg"),
                            ),
                            const SizedBox(
                              height: 9.0,
                            ),
                            const Text(
                              "Toy Shop",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                        Column(
                          // ignore: prefer_const_literals_to_create_immutables
                          children: [
                            const CircleAvatar(
                                radius: 30,
                                backgroundImage:
                                    AssetImage("lib/assets/car3.jpg")),
                            const SizedBox(
                              height: 9.0,
                            ),
                            const Text(
                              "Car & Bike",
                              style: TextStyle(
                                  fontSize: 13.0, fontWeight: FontWeight.bold),
                            )
                          ],
                        ),
                      ],
                    )
                  ],
                ),
              )
            ],
          )),
    );
  }
}
//Third Page

import 'package:awesome_icons/awesome_icons.dart';
import 'package:flutter/material.dart';

class ThirdPage extends StatelessWidget {
  const ThirdPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.deepPurple.shade100,
      body: Padding(
        padding: const EdgeInsets.only(
          left: 10.0,
          right: 10.0,
          top: 10.0,
        ),
        child: ListView(
          // ignore: sort_child_properties_last
          children: [
            Container(
              height: 250,
              width: 380,
              decoration: BoxDecoration(
                  color: Colors.white,
                  borderRadius: BorderRadius.circular(10.0)),
              child: Column(
                children: [
                  Padding(
                    padding: const EdgeInsets.all(4.0),
                    child: Container(
                      decoration: BoxDecoration(
                          color: Colors.cyan[50],
                          borderRadius: BorderRadius.circular(10.0)),
                      height: 150,
                      width: 400,
                      child: Column(
                        crossAxisAlignment: CrossAxisAlignment.start,
                        children: [
                          const SizedBox(
                            height: 5.0,
                          ),
                          const Padding(
                            padding: EdgeInsets.only(left: 12.0),
                            child: Text("Vehicle Insurance"),
                          ),
                          const SizedBox(
                            height: 14.0,
                          ),
                          Padding(
                            padding:
                                const EdgeInsets.only(left: 10.0, right: 10.0),
                            child: TextField(
                              decoration: InputDecoration(
                                  hintText: "Enter Vehicle  Number",
                                  border: OutlineInputBorder(
                                      borderRadius:
                                          BorderRadius.circular(20.0))),
                            ),
                          ),
                        ],
                      ),
                    ),
                  ),
                  const Text("Or Brower By Vehicle Type"),
                  const SizedBox(height: 10.0),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    children: [
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Icon(
                            Icons.bike_scooter,
                            color: Colors.deepPurple,
                            size: 30.0,
                          ),
                          const Text("Bike")
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.car_crash,
                            color: Colors.deepPurple,
                            size: 30.0,
                          ),
                          Text("Car")
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.auto_awesome,
                            color: Colors.deepPurple,
                            size: 30.0,
                          ),
                          Text("Auto")
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.taxi_alert,
                            color: Colors.deepPurple,
                            size: 30.0,
                          ),
                          Text("Taxi")
                        ],
                      )
                    ],
                  )
                ],
              ),
            ),
            const SizedBox(
              height: 8.0,
            ),
            Container(
              height: 120,
              width: 380,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10.0),
                color: Colors.white,
              ),
              child: Column(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: [
                  const Text("Life and Accident"),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    children: [
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            FontAwesomeIcons.handshakeAltSlash,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Term Life"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.drive_eta,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Accident"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.restaurant,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Restorant"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            FontAwesomeIcons.vaadin,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Returns"),
                        ],
                      )
                    ],
                  )
                ],
              ),
            ),
            const SizedBox(
              height: 8.0,
            ),
            Container(
              height: 120,
              width: 380,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10.0),
                color: Colors.white,
              ),
              child: Column(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: [
                  const Text("Health"),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    children: [
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.health_and_safety,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Health++"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.coronavirus_rounded,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Covid-19"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.superscript_outlined,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("SuperScript "),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            FontAwesomeIcons.angleRight,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("AngleUp"),
                        ],
                      )
                    ],
                  )
                ],
              ),
            ),
            const SizedBox(
              height: 8.0,
            ),
            Container(
              height: 120,
              width: 380,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10.0),
                color: Colors.white,
              ),
              child: Column(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: [
                  const Text("Travle and Others"),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    children: [
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            FontAwesomeIcons.facebookF,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("FaceBook"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.flight,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Flight"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.shop,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Shops"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            FontAwesomeIcons.mobile,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Mobile"),
                        ],
                      )
                    ],
                  )
                ],
              ),
            ),
            const SizedBox(
              height: 10.0,
            ),
            SingleChildScrollView(
              scrollDirection: Axis.horizontal,
              child: Row(
                children: [
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.teal),
                    child: Card(
                        child: Image.asset("lib/assets/car1.jpg",
                            fit: BoxFit.cover)),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.orange),
                    child: Card(
                      child: Image.asset(
                        "lib/assets/car2.jpg",
                        fit: BoxFit.cover,
                      ),
                    ),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.green),
                    child: Card(
                      child: Image.asset(
                        "lib/assets/car4.jpg",
                        fit: BoxFit.cover,
                      ),
                    ),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.cyan),
                    child: Card(
                      child: Image.asset(
                        "lib/assets/train.jpg",
                        fit: BoxFit.cover,
                      ),
                    ),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.pink),
                    child: Card(
                        child: Image.asset("lib/assets/flight.jpg",
                            fit: BoxFit.cover)),
                  )
                ],
              ),
            ),
          ],
          physics: const BouncingScrollPhysics(),
        ),
      ),
    );
  }
}
// Forth Page
import 'package:flutter/material.dart';
import 'package:awesome_icons/awesome_icons.dart';
// import 'package:flutter/physics.dart';

class FourthPage extends StatelessWidget {
  const FourthPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.deepPurple.shade100,
      body: Padding(
        padding: const EdgeInsets.all(10.0),
        child: ListView(
          physics: const BouncingScrollPhysics(),
          children: [
            const SizedBox(
              height: 10.0,
            ),
            TextField(
              decoration: InputDecoration(
                  filled: true,
                  fillColor: Colors.white,
                  border: OutlineInputBorder(
                      borderRadius: BorderRadius.circular(33.0)),
                  prefixIcon: const Icon(Icons.search_outlined),
                  hintText: "Search by store name or phone number",
                  hintStyle: const TextStyle(fontSize: 16.0)),
            ),
            const SizedBox(
              height: 10.0,
            ),
            Container(
              height: 140,
              width: 380,
              decoration: BoxDecoration(
                  color: Colors.white,
                  borderRadius: BorderRadius.circular(10.0)),
              child: Padding(
                padding: const EdgeInsets.all(10.0),
                child: Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: [
                    const Text(
                      "Create Wealth with SIP",
                      style: TextStyle(fontSize: 20.0),
                    ),
                    const Text("4.5 Cr+ Sip investemetn every month"),
                    const Text("Grow Your money SIP now"),
                    const SizedBox(
                      height: 10.0,
                    ),
                    ElevatedButton(
                      onPressed: () {},
                      // ignore: sort_child_properties_last
                      child: const Text("START A SIP     >"),
                      style: ElevatedButton.styleFrom(
                          shape: const StadiumBorder()),
                    )
                  ],
                ),
              ),
            ),
            const SizedBox(
              height: 10.0,
            ),
            Container(
              // margin: const EdgeInsets.all(8.0),
              decoration: BoxDecoration(
                  color: Colors.white,
                  borderRadius: BorderRadius.circular(10.0)),
              height: 250,
              width: 300,
              child: Column(
                children: [
                  const SizedBox(
                    height: 10,
                  ),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceAround,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      const Text(
                        'Insurance',
                        style: TextStyle(
                            fontWeight: FontWeight.bold, fontSize: 20),
                      ),
                    ],
                  ),
                  const SizedBox(
                    height: 10,
                  ),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      const Icon(
                        Icons.h_mobiledata,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                      const Icon(
                        FontAwesomeIcons.car,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                      const Icon(
                        Icons.health_and_safety,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                      const Icon(
                        FontAwesomeIcons.personBooth,
                        size: 40,
                        color: Colors.deepPurple,
                      )
                    ],
                  ),
                  const SizedBox(
                    height: 7,
                  ),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      const Text("      Bike \n     "),
                      const SizedBox(
                        width: 4,
                      ),
                      const Text(
                        'Car',
                        style: TextStyle(),
                      ),
                      const Text("Health++"),
                      const Text("    Person\n Accident")
                    ],
                  ),
                  const SizedBox(
                    height: 10,
                  ),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    children: [
                      const Icon(
                        FontAwesomeIcons.houseDamage,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                      const Icon(
                        FontAwesomeIcons.wineBottle,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                      const Icon(
                        Icons.cast_for_education_rounded,
                        size: 40,
                        color: Colors.deepPurple,
                      ),
                      Container(
                        height: 50,
                        width: 50,
                        decoration: BoxDecoration(
                            borderRadius: BorderRadius.circular(10.0),
                            color: Colors.deepPurple),
                        child: const Icon(
                          Icons.arrow_back_ios_new_sharp,
                          size: 20,
                          color: Colors.white,
                        ),
                      )
                    ],
                  ),
                  const SizedBox(
                    height: 10,
                  ),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    // ignore: prefer_const_literals_to_create_immutables
                    children: [
                      const Text("          Rent \n      Payment"),
                      const SizedBox(
                        width: 4,
                      ),
                      const Text(
                        '         Loan \n     RePayment',
                        style: TextStyle(),
                      ),
                      const Text("       Education\n         Fees"),
                      const Text("     See All \n                             ")
                    ],
                  ),
                ],
              ),
            ),
            const SizedBox(
              height: 10.0,
            ),
            Container(
              height: 120,
              width: 380,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10.0),
                color: Colors.white,
              ),
              child: Column(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: [
                  const Text("Life and Accident"),
                  Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    children: [
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            FontAwesomeIcons.handshakeAltSlash,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Term Life"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.drive_eta,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Accident"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            Icons.restaurant,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Restorant"),
                        ],
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                        children: const [
                          Icon(
                            FontAwesomeIcons.vaadin,
                            size: 30,
                            color: Colors.deepPurple,
                          ),
                          Text("Returns"),
                        ],
                      )
                    ],
                  )
                ],
              ),
            ),
            const SizedBox(
              height: 10.0,
            ),
            SingleChildScrollView(
              scrollDirection: Axis.horizontal,
              child: Row(
                children: [
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.teal),
                    child: Card(
                        child: Image.asset("lib/assets/car1.jpg",
                            fit: BoxFit.cover)),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.orange),
                    child: Card(
                      child: Image.asset(
                        "lib/assets/car2.jpg",
                        fit: BoxFit.cover,
                      ),
                    ),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.green),
                    child: Card(
                      child: Image.asset(
                        "lib/assets/car4.jpg",
                        fit: BoxFit.cover,
                      ),
                    ),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.cyan),
                    child: Card(
                      child: Image.asset(
                        "lib/assets/train.jpg",
                        fit: BoxFit.cover,
                      ),
                    ),
                  ),
                  Container(
                    // padding: EdgeInsets.only(right: 10, left: 10),
                    margin: const EdgeInsets.only(left: 10.0, right: 10.0),
                    height: 150,
                    width: 370,
                    decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(10.0),
                        color: Colors.pink),
                    child: Card(
                        child: Image.asset("lib/assets/flight.jpg",
                            fit: BoxFit.cover)),
                  )
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
// Fifth Page

import 'package:awesome_icons/awesome_icons.dart';
import 'package:flutter/material.dart';

class FifthPage extends StatelessWidget {
  const FifthPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        backgroundColor: Colors.deepPurple.shade100,
        body: Padding(
          padding: const EdgeInsets.only(left: 10, right: 10, top: 10),
          child: Container(
            height: double.infinity,
            width: double.infinity,
            decoration: BoxDecoration(
                color: Colors.white, borderRadius: BorderRadius.circular(10.0)),
            child: ListView(
              children: [
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(
                      Icons.electric_bolt,
                      color: Colors.white,
                      size: 30,
                    ),
                  ),
                  title: const Text("Mobile Recharge for"),
                  subtitle: const Text("6352006349"),
                  trailing: const Text(
                    "200",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    30 Day ago'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Failed "),
                          const Icon(FontAwesomeIcons.question)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                     const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
                ListTile(
                  leading: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(20.0),
                      color: Colors.deepPurple,
                    ),
                    height: 50,
                    width: 50,
                    child: const Icon(Icons.arrow_downward_outlined),
                  ),
                  title: const Text("Received From"),
                  subtitle: const Text("R"),
                  trailing: const Text(
                    "2000",
                    style: TextStyle(fontSize: 30.0),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.all(8.0),
                  child: Row(
                    mainAxisAlignment: MainAxisAlignment.spaceBetween,
                    children: [
                      const Text('    1 Day'),
                      Row(
                        // ignore: prefer_const_literals_to_create_immutables
                        children: [
                          const Text("Credited to "),
                          const Icon(FontAwesomeIcons.exclamation)
                        ],
                      )
                    ],
                  ),
                ),
                const Divider(
                  thickness: 2.0,
                ),
              ],
            ),
          ),
        ));
  }
}
// First Page Navigation

import 'package:flutter/material.dart';
// import 'package:awesome_icons/awesome_icons.dart';

class ToMobile extends StatelessWidget {
  const ToMobile({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.deepPurple.shade100,
      appBar: AppBar(
        title: const Text("Send Money"),
      ),
      body: Padding(
        padding: const EdgeInsets.all(8.0),
        child: SingleChildScrollView(
          child: Column(
            children: [
              const SizedBox(
                height: 8.0,
              ),
              TextField(
                decoration: InputDecoration(
                    filled: true,
                    fillColor: Colors.white,
                    border: OutlineInputBorder(
                        borderRadius: BorderRadius.circular(33.0)),
                    prefixIcon: const Icon(Icons.search_outlined),
                    hintText: "Search by store name or phone number",
                    hintStyle: const TextStyle(fontSize: 16.0)),
              ),
              const SizedBox(
                height: 10.0,
              ),
              Container(
                height: 584.0,
                width: 370.0,
                decoration: BoxDecoration(
                    color: Colors.white,
                    borderRadius: BorderRadius.circular(10.0)),
                child: ListView(
                  // ignore: prefer_const_literals_to_create_immutables
                  children: [
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        child: Text(
                          "R",
                          style: TextStyle(
                            fontSize: 25,
                            color: Colors.white,
                          ),
                        ),
                      ),
                      title: Text(
                        "R",
                        style: TextStyle(
                          fontSize: 20.0,
                        ),
                      ),
                      subtitle: Text(
                        "2000 -Received Instantly",
                      ),
                      trailing: Text(
                        "07/02",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        backgroundImage: AssetImage("lib/assets/car1.jpg"),
                      ),
                      title: Text("Pappu Pal",
                          style: TextStyle(fontWeight: FontWeight.bold)),
                      subtitle: Text("You: Sharedd a transacatin receipt"),
                      trailing: Text(
                        "26/12",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        child: Text(
                          "P",
                          style: TextStyle(
                            fontSize: 25,
                            color: Colors.white,
                          ),
                        ),
                      ),
                      title: Text(
                        "Suraj yadav",
                        style: TextStyle(fontWeight: FontWeight.bold),
                      ),
                      subtitle: Text("10 - Received instantly"),
                      trailing: Text(
                        "04/02",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        child: Text(
                          "P",
                          style: TextStyle(
                            fontSize: 25,
                            color: Colors.white,
                          ),
                        ),
                      ),
                      title: Text(
                        "Suraj yadav",
                        style: TextStyle(fontWeight: FontWeight.bold),
                      ),
                      subtitle: Text("10 - Received instantly"),
                      trailing: Text(
                        "04/02",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        backgroundImage: AssetImage("lib/assets/car1.jpg"),
                      ),
                      title: Text("Pappu Pal",
                          style: TextStyle(fontWeight: FontWeight.bold)),
                      subtitle: Text("You: Sharedd a transacatin receipt"),
                      trailing: Text(
                        "26/12",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        backgroundImage: AssetImage("lib/assets/car1.jpg"),
                      ),
                      title: Text("Pappu Pal",
                          style: TextStyle(fontWeight: FontWeight.bold)),
                      subtitle: Text("You: Sharedd a transacatin receipt"),
                      trailing: Text(
                        "26/12",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        child: Text(
                          "P",
                          style: TextStyle(
                            fontSize: 25,
                            color: Colors.white,
                          ),
                        ),
                      ),
                      title: Text(
                        "Suraj yadav",
                        style: TextStyle(fontWeight: FontWeight.bold),
                      ),
                      subtitle: Text("10 - Received instantly"),
                      trailing: Text(
                        "04/02",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        child: Text(
                          "P",
                          style: TextStyle(
                            fontSize: 25,
                            color: Colors.white,
                          ),
                        ),
                      ),
                      title: Text(
                        "Suraj yadav",
                        style: TextStyle(fontWeight: FontWeight.bold),
                      ),
                      subtitle: Text("10 - Received instantly"),
                      trailing: Text(
                        "04/02",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        child: Text(
                          "P",
                          style: TextStyle(
                            fontSize: 25,
                            color: Colors.white,
                          ),
                        ),
                      ),
                      title: Text(
                        "Suraj yadav",
                        style: TextStyle(fontWeight: FontWeight.bold),
                      ),
                      subtitle: Text("10 - Received instantly"),
                      trailing: Text(
                        "04/02",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                    const Divider(
                      thickness: 2.0,
                    ),
                    const ListTile(
                      leading: CircleAvatar(
                        radius: 30,
                        child: Text(
                          "P",
                          style: TextStyle(
                            fontSize: 25,
                            color: Colors.white,
                          ),
                        ),
                      ),
                      title: Text(
                        "Suraj yadav",
                        style: TextStyle(fontWeight: FontWeight.bold),
                      ),
                      subtitle: Text("10 - Received instantly"),
                      trailing: Text(
                        "04/02",
                        style: TextStyle(fontSize: 20.0),
                      ),
                    ),
                  ],
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
// image name
