# expand-category-sakai

##ライセンス
WordpressなんでGPL2です。

##利用規約
http://www.webopixel.net/wordpress/436.html
こちらの記事の管理人に許可をもらって丸コピしたので
制作した本人も理解してないところが多々あります。
利用は自己責任でお願いします。
利用は自己責任でお願いします。
大切なことなので2回書きました。

今のところwordpress.orgに上げるつもりがあります。


##設置サンプル


### 例1　サイドバーに表示
sidebar.php
```
	<?php
	if ($category = get_the_category()):
?>
<aside class="widget">
		foreach ($category as $value) {
			$cat_data = get_option('cat_'.intval($value->term_id));
			print_r($cat_data['extra_text']);
		}
</aside>
	<?php
	endif;
	?>
```

### 例2　記事本文中に挿入
```
	[exc-sakai]
```
