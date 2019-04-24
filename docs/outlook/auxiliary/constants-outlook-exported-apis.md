---
title: (Outlook エクスポート Api) 定数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: このトピックでは、Outlook でエクスポートされる api の定数定義について説明します。
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319874"
---
# <a name="constants-outlook-exported-apis"></a>(Outlook エクスポート Api) 定数

このトピックでは、Outlook でエクスポートされる api の定数定義について説明します。
  
## <a name="definitions-for-time-zone-support"></a>タイムゾーンサポートの定義

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>カテゴリサポートの定義

|**定数**|**定義**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>その他のディスパッチ識別子

Outlook では、次のディスパッチ識別子 (dispid) が公開されているため、開発者は[IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)を使用して、対応するプロパティやメソッドにアクセスしたり、対応するイベントを聞いたりすることができます。 
  
|**関連する定数**|**Dispid 値**|**説明**|**適用可能なインターフェイス**|
|:-----|:-----|:-----|:-----|
|**dispidfdirty** <br/> |0xf024  <br/> |アイテムの対応するプロパティを呼び出して、アイテムが変更されたが保存されていないかどうかを確認するために使用します。  <br/> |アイテムレベルのオブジェクト  <br/> |
|**dispidShowSenderPhoto** <br/> |0xf・0  <br/> |指定した引数に基づいて連絡先の画像を表示するかどうかを指定するために、エクスプローラーまたはインスペクターの対応するメソッドを呼び出すために使用します。  <br/> |エクスプローラーまたはインスペクター  <br/> |
|**dispidbeforeprint** <br/> |0xFC8E  <br/> |**IDispatch:: Invoke**関数からのイベントを処理するために使用します。このイベントは、印刷操作の前に発生します。  <br/> |アプリケーション  <br/> |
|**dispidEventReadComplete** <br/> |0xfc8f  <br/> |Outlook がアイテムのプロパティの読み取りを完了したときに発生する**IDispatch:: Invoke**関数からのイベントを処理するために使用されます。  <br/> |アイテムレベルのオブジェクト  <br/> |
   
## <a name="see-also"></a>関連項目

- [Outlook でエクスポートされている API](outlook-exported-apis.md)
- [Outlook によりエクスポートされる API について](about-apis-exported-by-outlook.md)
- [Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [使用可能なイベントの dispid (Outlook エクスポート Api)](available-events-and-their-dispids-outlook-exported-apis.md)

