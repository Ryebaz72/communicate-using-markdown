# H1 Header

## H2 Header

### H3 Header

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

``` go

http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
		names := r.URL.Query()["name"]
		var name string
		if len(names) == 1 {
			name = names[0]
		}
		//w.Write([]byte("Hello " + name))
		m := map[string]string{"name": name}
		enc := json.NewEncoder(w)
		enc.Encode(m)
	})

	err := http.ListenAndServe(":3000", nil)

	if err != nil {
		log.Fatal(err)
  ```
