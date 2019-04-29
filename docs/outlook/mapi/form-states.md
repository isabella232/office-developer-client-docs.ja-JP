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
  
フォームオブジェクトは、どのメソッドが呼び出されたか、およびそれらのメソッドの実行時にエラーが発生したかどうかに応じて、5つの異なる状態のいずれかになります。 これらの状態については、以下のトピックで説明します。
  
- [未初期化状態](uninitialized-state.md)
    
- [通常の状態](normal-state.md)
    
- [noscribble 状態](noscribble-state.md)
    
- [保存の状態を処理する](handsoffaftersave-state.md)
    
- [標準の状態](handsofffromnormal-state.md)
    
状態は、主に form オブジェクト内のデータの状態に関連しています。 さまざまな状態は、データを保存する必要があるかどうか、フォームオブジェクトがデータに変更を加えることができるかどうか、およびフォームがどのようなデータを保存するかを表します。 そのため、フォームの状態と、それらの間の切り替えは、フォームサーバーの IPersistMessage の実装とは他のものよりも、 [IUnknown](ipersistmessageiunknown.md)インターフェイスメソッドの実装によって大きくなります。 これらの状態に関する知識は、フォームサーバーで実装する必要がある MAPI フォームインターフェイスを適切に実装するのに非常に役立ちます。 
  
このセクションのトピックでは、さまざまな状態と、他の状態に遷移する可能性がある許可されるアクションについて説明します。 これらのトピックに記載されていない遷移は許可されません。 フォームオブジェクトで状態間の移行が許可されない場合は、メッセージングクライアントが予期している方法では動作せず、予期しないクライアントまたはフォームオブジェクトの動作が発生する可能性があります。
  
> [!NOTE]
> 一部の状態遷移は、以前の状態の情報に依存します。 フォームサーバーでは、多くの場合、メッセージのプロパティの値が変更されているかどうかを示すフラグを form オブジェクトに実装する必要があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI フォームサーバーの開発](developing-mapi-form-servers.md)

