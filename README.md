### EX5 Information Retrieval Using Boolean Model in Python
### DATE: 
### AIM: To implement Information Retrieval Using Boolean Model in Python.
### Description:
<div align = "justify">
The Boolean model in Information Retrieval (IR) is a fundamental model used for searching and retrieving information from a collection of documents. It operates on the principles of set theory and logic, where documents are represented as sets of terms or words, and queries are expressed as Boolean expressions using logical operators such as AND, OR, and NOT.
  
### Procedure:
1. ***Initialize the BooleanRetrieval class:*** The BooleanRetrieval class is defined to manage the indexing and searching of documents.
2. ***Constructor and Index Initialization:*** The class constructor initializes an empty index to store the inverted index mapping terms to documents.
3. ***Indexing Documents:***
    <p> a) The index_document method is responsible for indexing documents.
    <p> b) Tokenize the text content of documents, converting them into lowercase terms.
    <p> c) For each term in the document, it adds an entry in the index, associating the term with the document ID. </p>
4. ***Fetch Web Page Text:***
    <p>a) The fetch_webpage_text method uses the requests library to fetch content from a given URL.
    <p>b) Extract text content from the fetched HTML using BeautifulSoup.
    <p>c) The extracted text is returned for further processing.
5. ***Boolean Search:***
    <p>a) The boolean_search method performs Boolean searches on the indexed documents.
    <p>b) Tokenize the input query and iterates through its terms.
    <p>c) For each term in the query, it retrieves documents containing that term and performs Boolean operations (AND, OR, NOT) based on the query's structure.

### Program:

if __name__ == "__main__":
    indexer = BooleanRetrieval()

   
    documents = {
        1: "Python is a programming language",
        2: "Information retrieval deals with finding information",
        3: "Boolean models are used in information retrieval"
    }

    for doc_id, text in documents.items():
        indexer.index_document(doc_id, text)

    
    indexer.create_documents_matrix(documents)
    indexer.print_documents_matrix_table()


    indexer.print_all_terms()


    query1 = input("Enter your boolean query: ")
    results = indexer.boolean_search(query1)
    if results:
        print(f"\nResults for '{query1}': {results}")
    else:
        print("No results found for the query.")


# Example usage:
if __name__ == "__main__":
    indexer = BooleanRetrieval()

   
    documents = {
        1: "Python is a programming language",
        2: "Information retrieval deals with finding information",
        3: "Boolean models are used in information retrieval"
    }

    for doc_id, text in documents.items():
        indexer.index_document(doc_id, text)

    
    indexer.create_documents_matrix(documents)
    indexer.print_documents_matrix_table()


    indexer.print_all_terms()


    query1 = input("Enter your boolean query: ")
    results = indexer.boolean_search(query1)
    if results:
        print(f"\nResults for '{query1}': {results}")
    else:
        print("No results found for the query.")


### Output:
<img width="860" alt="image" src="https://github.com/user-attachments/assets/2f26c448-827a-499c-bdb6-06ad8c272bab">


### Result:
Thus, the implementation of Information Retrieval using Boolean model had been successfully done using python.
