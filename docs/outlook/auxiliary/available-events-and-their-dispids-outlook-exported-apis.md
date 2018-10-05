---
title: 使用可能なイベントの dispid (Outlook エクスポート Api)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: このセクションでは、Outlook で使用可能なイベントのディスパッチ識別子について説明します。
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400237"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>使用可能なイベントの dispid (Outlook エクスポート Api)

このセクションでは、Outlook で使用可能なイベントのディスパッチ識別子について説明します。
  
Outlook では、聴くし、 [:invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)関数の対応するイベントを処理する C++ のアドインを使用するのには次のディスパッチ識別子 (dispid) を公開します。 
  
|**定数**|**イベントの Dispid**|**説明**|**パラメーター**|**解説**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |印刷操作の前に起動する **:invoke**関数からアプリケーション レベルのイベントを処理するために使用されます。  <br/> | 2 つの名前のないパラメーターがあります。  <br/>  型の最初のパラメーターは、* * VT_BOOL|VT_BREF *。 **VARIANT_TRUE**をは、イベントをキャンセルするには、このパラメーターに返されます。  <br/>  2 番目のパラメーターは使用しない、無視してください。  <br/> |この dispid は、Outlook 2010 以降に使用できます。  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Outlook がアイテムのプロパティの読み取りを完了したときに発生する **:invoke**関数からのアイテム レベルのイベントを処理するために使用されます。  <br/> |_キャンセル_型のパラメーターが 1 つだけ * * VT_BOOL|VT_BREF *。 **VARIANT_TRUE**をは、読み取り操作をキャンセルするには、このパラメーターに返されます。  <br/> |この dispid は、Outlook 2010 以降に使用できます。  <br/> このイベントは、 **IExchExtMessageEvents::OnReadComplete**では、Exchange クライアント拡張機能 (ECE) のイベントに対応しも**ReadComplete**イベントに追加されたオブジェクト モデルに Outlook 2013 以降です。  <br/> |
   
Dispid を使用して聴くし、イベントを処理する方法の例を参照してください、`CAppEventListener::Invoke`関数は、C++ の Outlook ソリューションでは[MFC C 2003 .NET で Outlook 2002/XP イベント シンクを実装する](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)」に記載します。
  
## <a name="see-also"></a>関連項目

- [Outlook でエクスポートされている API](outlook-exported-apis.md)
- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [Outlook によりエクスポートされる API について](about-apis-exported-by-outlook.md)
- [MFC C 2003 .NET のシンクを Outlook 2002/XP のイベントを実装します。](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

