---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286629"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームビューアーの状態で変更が発生したことを示します。 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>パラメーター

 _uldir_
  
> 順番viewer で発生した変更に関する情報と、フォームで想定される応答を提供するフラグのビットマスク。 次のフラグを設定できます。
    
VCSTATUS_CATEGORY 
  
> 別のカテゴリに、次または前のメッセージがあります。 
    
VCSTATUS_INTERACTIVE 
  
> フォームにユーザーインターフェイスが表示されます。 このフラグが設定されていない場合、通常、ユーザーインターフェイスが表示される原因となる動詞に応答している場合でも、フォームはユーザーインターフェイスを表示しません。 
    
VCSTATUS_MODAL 
  
> フォームビューアーのモーダルにします。 
    
VCSTATUS_NEXT 
  
> フォームビューアーに次のメッセージがあります。 
    
VCSTATUS_PREV 
  
> フォームビューアーに前のメッセージがあります。 
    
VCSTATUS_READONLY 
  
> Delete、submit、および move 操作を無効にする必要があります。 
    
VCSTATUS_UNREAD 
  
> フォームビューアーに、次または前の未読メッセージがあります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知は正常に実行されました。
    
## <a name="remarks"></a>解説

フォームビューアーは**IMAPIFormAdviseSink:: OnChange**メソッドを呼び出して、閲覧者のステータスの変更についてフォームに通知します。 通常、この変更は、閲覧者の次または前のメッセージが存在するかどうかに基づいて、VCSTATUS_NEXT または VCSTATUS_PREVIOUS フラグを設定またはクリアすることだけです。 そのため、form オブジェクトは、サポートする次または前のアクションを有効または無効にします。 
  
VCSTATUS_MODAL および VCSTATUS_INTERACTIVE の設定は、作成後にビューコンテキストで変更することはできません。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

このメソッドの具体的な実装は、フォームの仕様に完全に依存しています。 ほとんどの form オブジェクトは、このメソッドを使用してユーザーインターフェイスを変更します (たとえば、メニューコマンドやボタンを有効または無効にしてビューア状態フラグパラメーターに一致させる)。
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

