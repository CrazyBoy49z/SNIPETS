# SNIPETS
SNIPETS MIGX, MODX, PHP, JS, JQ, CSS, PYTHON, HTML

MIGX inputs
------------------
-- Content tabs --
------------------
    [
      {"caption":"", "fields": [
        {"field":"title","caption":"h2 Название"},
        {"field":"text","caption":"Текст"},
        {"field":"description","caption":"Description","inputTV":"richtext"},
        {"field":"img", "caption":"Изображение", "inputTVtype":"image"},
        {"field":"list1","caption":"Выбор из списка","inputTVtype":"listbox","inputOptionValues":"первый==1||втоорой==2||третий==3"}
      ]}
    ]
------------------------
-- Content of columns --
------------------------
    [
        {"header": "1", "width": "160", "sortable": "true", "dataIndex": "title"},
        {"header": "2", "width": "160", "sortable": "true", "dataIndex": "text"},
        {"header": "3", "width": "160", "sortable": "true", "dataIndex": "description"},
        {"header": "4", "width": "160", "sortable": "true", "dataIndex": "img"},
        {"header": "5", "width": "160", "sortable": "true", "dataIndex": "list1"}
    ]
    
----------------------------
-- Call to inputs on page --
----------------------------
    [[getImageList?
        &tvname=`features-icon-text` // TV inputs
        &tpl=`features-icon-text`    // Chunk
        &docid=`1`
        &where=`{'':''}`
    ]]
