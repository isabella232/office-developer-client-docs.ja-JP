---
title: (Outlook でエクスポートされた Api) の定数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: このトピックには、Outlook にエクスポートする Api の定数の定義が含まれています。
ms.openlocfilehash: 54b491e436b7b9275a227de40439ddb66d8d0c5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799304"
---
# <a name="constants-outlook-exported-apis"></a>(Outlook でエクスポートされた Api) の定数

このトピックには、Outlook にエクスポートする Api の定数の定義が含まれています。
  
## <a name="definitions-for-time-zone-support"></a>タイム ゾーンの定義をサポートします。

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>カテゴリの定義をサポートします。

|**定数**|**定義**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>その他のディスパッチ識別子

開発者は、対応するプロパティまたはメソッドにアクセスしたり、対応するイベントを待機する[:invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx)を使用できるように、outlook は次のディスパッチ識別子 (dispid) を公開します。 
  
|**関連付けられた定数**|**Dispid 値**|**説明**|**適用可能なインタ フェース**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |アイテムが変更されていますが保存されていないかどうかを確認する項目に対応するプロパティを呼び出すために使用します。  <br/> |アイテム レベルのオブジェクト  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |指定された引数に基づいて、連絡先の画像を表示するかどうかを指定するのには、エクスプ ローラーまたはインスペクターの対応するメソッドを呼び出すために使用します。  <br/> |エクスプ ローラーまたはインスペクター  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |印刷操作の前に起動する **:invoke**関数からイベントを処理するために使用されます。  <br/> |アプリケーション  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Outlook がアイテムのプロパティの読み取りを完了したときに発生する **:invoke**関数からイベントを処理するために使用されます。  <br/> |アイテム レベルのオブジェクト  <br/> |
   
## <a name="see-also"></a>関連項目

- [Outlook は、Api をエクスポートします。](outlook-exported-apis.md)
- [Outlook によってエクスポートされた Api について](about-apis-exported-by-outlook.md)
- [Outlook アイテムが変更されたが、(Outlook の補助参照) が保存されていないかどうかを決定します。](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [(Outlook の補助参照) を Outlook で連絡先の画像を表示するかどうかを指定します。](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
- [使用可能なイベントの dispid (Outlook エクスポート Api)](available-events-and-their-dispids-outlook-exported-apis.md)

