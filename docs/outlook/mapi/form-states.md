---
title: フォームの状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 195a82bfcc163ee01d2d42c71e79a8f5c9c620e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564634"
---
# <a name="form-states"></a>フォームの状態

**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム オブジェクトは、それらにどのようなメソッドが呼び出された、およびそれらのメソッドを実行する際にエラーが発生しているかどうかによって、5 つの異なる状態のいずれかで指定できます。 状態は次のトピックで説明します。
  
- [Uninitialized 状態](uninitialized-state.md)
    
- [Normal 状態](normal-state.md)
    
- [NoScribble 状態](noscribble-state.md)
    
- [HandsOffAfterSave 状態](handsoffaftersave-state.md)
    
- [HandsOffFromNormal 状態](handsofffromnormal-state.md)
    
状態は、主に、フォーム オブジェクト内のデータの状態に関連します。 さまざまな状態では、フォーム オブジェクトは、データ、および、どの時点では、フォームでデータを保存する際に変更を許可する必要があるかどうかを保存するには、データが必要かどうかを反映します。 ように、フォームの状態およびそれらの間の遷移がある他の操作、フォームのサーバーの実装の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)よりも、他のメソッドのインターフェイスです。 これらの状態の知識は、フォーム サーバーを実装する必要があります、MAPI フォーム インターフェイスの適切な実装に非常に便利です。 
  
このセクションのトピックでは、他の状態への遷移が発生するを許可する操作と、さまざまな状態について説明します。 トピックに記載されていないすべての遷移を指定することはできません。 場合は、フォーム オブジェクトでは、[許可しない] の切り替えを行うための状態の間、メッセージング クライアントが予想され、クライアント、またはフォーム オブジェクトの予期しない動作が発生する可能性がありますの方法では動作しません。
  
> [!NOTE]
> いくつかの状態の遷移は、以前の状態からの情報に依存します。 フォーム サーバーは、後の状態の変更を容易にするメッセージのプロパティの値が変更されたかどうかを示すためには、そのフォーム オブジェクトにフラグを実装する可能性が高い必要があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

