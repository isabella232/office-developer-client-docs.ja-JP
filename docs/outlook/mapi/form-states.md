---
title: フォームの状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429167"
---
# <a name="form-states"></a>フォームの状態

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム オブジェクトは、呼び出されたメソッドと、それらのメソッドの実行でエラーが発生したかどうかに応じて、5 つの異なる状態の 1 つになります。 状態については、次のトピックで説明します。
  
- [初期化されていない状態](uninitialized-state.md)
    
- [標準状態](normal-state.md)
    
- [NoScribble 状態](noscribble-state.md)
    
- [HandsOffAfterSave 状態](handsoffaftersave-state.md)
    
- [HandsOffFromNormal State](handsofffromnormal-state.md)
    
状態は、主にフォーム オブジェクト内のデータの状態に関連します。 異なる状態は、データを保存する必要があるかどうか、フォーム オブジェクトがデータの変更を許可するかどうか、およびフォームが含まれるデータを保存する過程のポイントを反映します。 そのため、フォームの状態と切り替えは、フォーム サーバーの [IPersistMessage : IUnknown](ipersistmessageiunknown.md) インターフェイス メソッドの実装と他の方法よりも関係があります。 これらの状態に関する知識は、フォーム サーバーが実装する必要がある MAPI フォーム インターフェイスを適切に実装する場合に非常に役立ちます。 
  
このセクションのトピックでは、さまざまな状態と、他の状態への移行を引き起こす許可されるアクションについて説明します。 トピックに記載されていない遷移は許可されません。 フォーム オブジェクトが状態間の移行を許可しない場合、メッセージング クライアントが期待する方法では動作し、予期しないクライアントまたはフォーム オブジェクトの動作を引き起こす可能性があります。
  
> [!NOTE]
> 一部の状態遷移は、以前の状態からの情報に依存します。 フォーム サーバーは、メッセージのプロパティの値が変更されたかどうかを示すために、フォーム オブジェクトにフラグを実装して、後で状態を変更する必要があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

