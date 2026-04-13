import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'h4',
      // Light Mode with default background
      theme: ThemeData(
        primarySwatch: Colors.blue,
        brightness: Brightness.light,
      ),
      home: const MyHomePage(title: 'Car Product Listing'),
    );
  }
}

class MyHomePage extends StatelessWidget {
  const MyHomePage({Key? key, required this.title}) : super(key: key);
  final String title;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text(title)),
      body: ListView(
        padding: const EdgeInsets.symmetric(horizontal: 10.0, vertical: 15.0),
        children: const <Widget>[
          
          ProductBox(
            name: "Challenger Hellcat",
            brand: "Dodge",
            description: "Supercharged 6.2L HEMI V8 SRT Engine with 717 HP.",
            price: 85000,
            image: "hellcat.png",
          ),
        
          ProductBox(
            name: "Aventador SVJ",
            brand: "Lamborghini",
            description: "Naturally Aspirated V12 Engine, Top Speed 350 km/h.",
            price: 515000,
            image: "lamborghini.png",
          ),
        
          ProductBox(
            name: "812 Superfast",
            brand: "Ferrari",
            description: "800 cv output, high performance Italian luxury car.",
            price: 335000,
            image: "ferrari.png",
          ),
        
          ProductBox(
            name: "911 GT3",
            brand: "Porsche",
            description: "High-performance homologation model, track-focused.",
            price: 175000,
            image: "porsche.png",
          ),
        ],
      ),
    );
  }
}

class ProductBox extends StatelessWidget {
  const ProductBox({
    Key? key,
    required this.name,
    required this.brand,
    required this.description,
    required this.price,
    required this.image,
  }) : super(key: key);

  final String name;
  final String brand;
  final String description;
  final int price;
  final String image;

  @override
  Widget build(BuildContext context) {
    return Card(
      margin: const EdgeInsets.only(bottom: 12),
      elevation: 2,
      child: ExpansionTile(
        // The main title and leading image
        leading: Image.asset(
          "images/" + image,
          width: 50,
          errorBuilder: (context, error, stackTrace) => const Icon(Icons.directions_car),
        ),
        title: Text(
          "$brand $name",
          style: const TextStyle(fontWeight: FontWeight.bold),
        ),
        subtitle: const Text("Click for details"),
        
        // The drop-down content (Dropdown list details)
        children: <Widget>[
          Padding(
            padding: const EdgeInsets.all(16.0),
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: [
                Text("Product Name: $name", style: const TextStyle(fontSize: 16)),
                const SizedBox(height: 6),
                Text("Brand: $brand", 
                    style: const TextStyle(fontSize: 16, color: Colors.blue, fontWeight: FontWeight.w500)),
                const SizedBox(height: 6),
                Text("Description: $description", style: const TextStyle(fontSize: 14)),
                const SizedBox(height: 6),
                const Divider(),
                Text(
                  "Price: \$${price.toString()}",
                  style: const TextStyle(fontWeight: FontWeight.bold, color: Colors.green, fontSize: 18),
                ),
              ],
            ),
          ),
        ],
      ),
    );
  }
}
