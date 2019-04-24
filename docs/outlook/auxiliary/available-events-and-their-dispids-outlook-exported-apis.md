---
title: 使用可能なイベントの dispid (Outlook エクスポート Api)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: このセクションでは、Outlook によって使用可能になるイベントのディスパッチ識別子について説明します。
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316878"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>使用可能なイベントの dispid (Outlook エクスポート Api)

このセクションでは、Outlook によって使用可能になるイベントのディスパッチ識別子について説明します。
  
Outlook では、次のディスパッチ識別子 (dispid) が公開されており、C++ アドインは、 [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)関数から対応するイベントをリッスンし、処理することができます。 
  
|**定数**|**イベントの Dispid**|**説明**|**パラメーター**|**解説**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidbeforeprint** <br/> |0xFC8E  <br/> |**IDispatch:: Invoke**関数から印刷操作の前に発生するアプリケーションレベルのイベントを処理するために使用されます。  <br/> | 2つの無名パラメーターがあります。  <br/>  最初のパラメーターの型は、* * VT_BOOL です。|VT_BREF * *。 イベントを取り消すには、このパラメーターで**VARIANT_TRUE**を返します。  <br/>  2番目のパラメーターは使用されないため、無視する必要があります。  <br/> |この dispid は、Outlook 2010 以降で利用可能です。  <br/> |
|**dispidEventReadComplete** <br/> |0xfc8f  <br/> |Outlook がアイテムのプロパティの読み取りを完了したときに発生する**IDispatch:: Invoke**関数からのアイテムレベルのイベントを処理するために使用されます。  <br/> |VT_BOOL 型のパラメーターは__ 1 つだけです。|VT_BREF * *。 読み取り操作を取り消すには、このパラメーターで**VARIANT_TRUE**を返します。  <br/> |この dispid は、Outlook 2010 以降で利用可能です。  <br/> このイベントは、Exchange クライアント拡張機能 (ECE) イベントの**iexchextmessageevents:: onreadcomplete**、および Outlook 2013 以降のオブジェクトモデルに追加された**readcomplete**イベントに対応しています。  <br/> |
   
dispid を使用してイベントをリッスンして処理する方法の例については`CAppEventListener::Invoke` 、「 [MFC c++ 2003 .net での outlook 2002/XP イベントシンクの実装](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)」で説明されている C++ outlook ソリューションの関数を参照してください。
  
## <a name="see-also"></a>関連項目

- [Outlook でエクスポートされている API](outlook-exported-apis.md)
- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [Outlook によりエクスポートされる API について](about-apis-exported-by-outlook.md)
- [MFC C++ 2003 .net での Outlook 2002/XP イベントシンクの実装](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

