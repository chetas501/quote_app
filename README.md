# quotes
```
List<Quote> quotes = [
    Quote(author: 'Oscar Wilde', text: 'Be yourself; everyone else is already taken'),
    Quote(author: 'Oscar Wilde', text: 'I have nothing to declare except my genius'),
    Quote(author: 'Oscar Wilde', text: 'The truth is rarely pure and never simple')
  ];
```
  ##------------------------------------------------------------------------------------------- <br>
  ```
  quotes.map((quote) => QuoteCard(
          quote: quote,
          delete: () {
            setState(() {
              quotes.remove(quote);
            });
          }
        )).toList(),
  ```
  ##------------------------------------------------------------------------------------------- <br>
  ```
  class Quote {

  String text;
  String author;
  Quote({ this.text, this.author });
}
  ```
  ##------------------------------------------------------------------------------------------- <br>
  ```
  class QuoteCard extends StatelessWidget {

  final Quote quote;
  final Function delete;
  QuoteCard({ this.quote, this.delete });
```
```
  @override
  Widget build(BuildContext context) {
    return Card(
  
  FlatButton.icon(
                onPressed: delete,
                label: Text('delete quote'),
                icon: Icon(Icons.delete),
              )
            ],
```
