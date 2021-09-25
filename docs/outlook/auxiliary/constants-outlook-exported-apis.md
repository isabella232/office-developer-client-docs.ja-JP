---
title: (Outlook エクスポート Api) 定数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: このトピックでは、エクスポートする API の定数Outlookします。
ms.openlocfilehash: 0ba6c94ad8f4e5ed78d8f6b4e2ea56ba8258c4e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614466"
---
# <a name="constants-outlook-exported-apis"></a>(Outlook エクスポート Api) 定数

このトピックでは、エクスポートする API の定数Outlookします。
  
## <a name="definitions-for-time-zone-support"></a>タイム ゾーンのサポートの定義

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Category サポートの定義

|**定数**|**定義**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>その他のディスパッチ識別子

Outlook開発者が[IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)を使用して対応するプロパティまたはメソッドにアクセスしたり、対応するイベントをリッスンしたりできるよう、次のディスパッチ識別子 (dispids) を公開します。 
  
|**関連付けられた定数**|**Dispid 値**|**説明**|**適用可能なインターフェイス**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |アイテムの対応するプロパティを呼び出して、アイテムが変更されたが保存されていないかどうかを確認するために使用します。  <br/> |アイテム レベルのオブジェクト  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |エクスプローラーまたはインスペクターで対応するメソッドを呼び出して、指定した引数に基づいて連絡先の画像を表示するかどうかを指定するために使用します。  <br/> |エクスプローラーまたはインスペクター  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |印刷操作の前に発生する **IDispatch::Invoke** 関数からイベントを処理するために使用します。  <br/> |アプリケーション  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |アイテムのプロパティの読み取りが完了した場合に発生する **IDispatch::Invoke** 関数Outlook処理するために使用されます。  <br/> |アイテム レベルのオブジェクト  <br/> |
   
## <a name="see-also"></a>関連項目

- [Outlook でエクスポートされている API](outlook-exported-apis.md)
- [Outlook によりエクスポートされる API について](about-apis-exported-by-outlook.md)
- [Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [使用可能なイベントの dispid (Outlook エクスポート Api)](available-events-and-their-dispids-outlook-exported-apis.md)

