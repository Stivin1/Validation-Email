int index = 0;

            string Email = "bot@bk.ru";

            string IndexEmail = "";

            ObservableCollection<string> collection_email_index = new ObservableCollection<string>();

            Dictionary<string, string> directory_email_index = new Dictionary<string, string>();

            Dictionary<int, char> directory_array = new Dictionary<int, char>();

            Regex ExtensionEmailRegex = new Regex(@"\@bk.ru(w*)$|@bk.com(w*)$");

            MatchCollection matches = ExtensionEmailRegex.Matches(Email);

            for (int i = 0; i < Email.Length; i++)
            {
                directory_array.Add(i, Email[i]);
            }

            foreach (var list in directory_array.Where(t => t.Value == '@'))
            {
                index = list.Key;
            }

            foreach (var list in directory_array)
            {
                if (list.Key < index) IndexEmail += list.Value;
            }

            foreach (Match list in matches)
            {
                collection_email_index.Add(IndexEmail);
                collection_email_index.Add(list.Value);
            }
