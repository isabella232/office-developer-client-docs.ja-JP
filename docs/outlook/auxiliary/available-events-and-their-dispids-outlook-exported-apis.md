---
title: 使用可能なイベントの dispid (Outlook エクスポート Api)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: このセクションでは、使用できるイベントのディスパッチOutlook説明します。
ms.openlocfilehash: d226fa92e96fea9092990b7c5ee290ce2df2cdaf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568083"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>使用可能なイベントの dispid (Outlook エクスポート Api)

このセクションでは、使用できるイベントのディスパッチOutlook説明します。
  
Outlook、次のディスパッチ識別子 (dispids) を公開して、C++ アドインが[IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)関数の対応するイベントをリッスンして処理できます。 
  
|**定数**|**イベントの Dispid**|**説明**|**パラメーター**|**注釈**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |印刷操作の前に発生する **IDispatch::Invoke** 関数からアプリケーション レベルのイベントを処理するために使用します。  <br/> | 2 つの名前のないパラメーターがあります。  <br/>  最初のパラメーターは型 **VT_BOOL|VT_BREF**。 イベント **VARIANT_TRUE** を取り消す場合は、このパラメーターの値を返します。  <br/>  2 番目のパラメーターは使用されないので、無視する必要があります。  <br/> |この dispid は、2010 年Outlook使用できます。  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |アイテムのプロパティの読み取りが完了した場合に発生する **IDispatch::Invoke** 関数Outlookを処理するために使用されます。  <br/> |**VT_BOOL の型の  _Cancel_ パラメーターは 1 つVT_BOOL|VT_BREF**。 この **パラメーター VARIANT_TRUE** 値を返して、読み取り操作を取り消します。  <br/> |この dispid は、2010 年Outlook使用できます。  <br/> このイベントは、Exchange クライアント拡張機能 (ECE) イベント **IExchExtMessageEvents::OnReadComplete** に対応し、Outlook 2013 以降にオブジェクト モデルに追加された **ReadComplete** イベントにも対応します。  <br/> |
   
dispid を使用してイベントをリッスンして処理する方法の例については `CAppEventListener::Invoke` [、「MFC C++ 2003 .NET での Outlook 2002/XP](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)イベント シンクの実装」で説明されている C++ Outlook ソリューションの関数を参照してください。
  
## <a name="see-also"></a>関連項目

- [Outlook でエクスポートされている API](outlook-exported-apis.md)
- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [Outlook によりエクスポートされる API について](about-apis-exported-by-outlook.md)
- [MFC C++ 2003 Outlook 2002/XP イベント シンクの実装](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

