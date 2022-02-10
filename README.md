# 제목(메인화면)


''' C#

private string Checked_pageSize()
          {
            string pageSize = "&pageSize=";
            CheckBox[] pageSize_list = { pageSize50, pageSize100, pageSize200 };
            List<CheckBox> pageSize_checked_list = new List<CheckBox>();
            for (int i = 0; i < pageSize_list.Length; i++)
            {
                if (pageSize_list[i].Checked)
                    pageSize_checked_list.Add(pageSize_list[i]);
            }
            if (pageSize_checked_list.Count == 0)
            {
                pageSize = "";
                return pageSize;
            }

            for (int i = 0; i < pageSize_checked_list.Count; i++)
            {
                pageSize += pageSize_checked_list[i].Name.Replace("pageSize", "") + ";";
            }
            pageSize = pageSize.Substring(0, pageSize.Length - 1);
            return pageSize;
        }

'''
