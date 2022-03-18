## Flutter-watch-app-ui-design

A new Flutter project.

## Getting Started

<div>
  <img style="width: 250px;" src="https://user-images.githubusercontent.com/68488154/158930793-8d7cf41f-282d-46ef-9a4c-c58165915028.jpg" alt="">
  <img style="width: 250px;" src="https://user-images.githubusercontent.com/68488154/158930808-660fbe60-594b-4fe5-a684-abda3433212b.jpg" alt="">
  <img style="width: 250px;" src="https://user-images.githubusercontent.com/68488154/158930821-d4542283-3061-439a-9b7d-ee5ce75ba593.jpg" alt="">
  <img style="width: 250px;" src="https://user-images.githubusercontent.com/68488154/158931082-fab2577b-4eef-4f2f-89fa-11d9961628c3.jpg" alt="">
  <img style="width: 250px;" src="https://user-images.githubusercontent.com/68488154/158931095-92a2a784-df19-477a-87cb-83056ab5bc93.jpg" alt="">
  <img style="width: 250px;" src="https://user-images.githubusercontent.com/68488154/158930850-5fda21ce-d05e-40e0-8673-9781bb24495a.jpg" alt="">
</div>

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,samples, guidance on mobile development, and a full API reference.

#� �F�l�u�t�t�e�r�-�w�a�t�c�h�-�a�p�p�-�u�i�-�d�e�s�i�g�n�

### NestedScrollView

```
import 'package:flutter/material.dart';
import 'sectionone.dart';

class Myhomepage extends StatefulWidget {
  const Myhomepage({Key? key}) : super(key: key);

  @override
  State<Myhomepage> createState() => _MyhomepageState();
}

class _MyhomepageState extends State<Myhomepage> {
  @override
  Widget build(BuildContext context) {
    return SafeArea(
      child: Scaffold(
        body: NestedScrollView(
          physics: NeverScrollableScrollPhysics(),
          headerSliverBuilder: (context, isScolled) {
            return [
              SliverAppBar(
                collapsedHeight: 282,
                expandedHeight: 282,
                flexibleSpace: Sectionone(),
              )
            ];
          },
          body: Padding(
            padding: const EdgeInsets.all(20.0),
            child: Container(
              height: 500,
              color: Colors.blue,
              child: GridView.builder(
                  gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(
                    crossAxisCount: 2,
                    crossAxisSpacing: 10,
                    mainAxisSpacing: 10,
                  ),
                  itemCount: 110,
                  itemBuilder: (_, index) {
                    return Container(
                      child: Center(
                        child: Text(
                          "This is grid",
                          style: TextStyle(
                            color: Colors.white,
                          ),
                        ),
                      ),
                      color: Colors.black,
                    );
                  }),
            ),
          ),
        ),
      ),
    );
  }
}

```
