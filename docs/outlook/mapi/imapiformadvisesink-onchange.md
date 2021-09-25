---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4ed41bc702d6296d1c714e89f99e9fac63ca055d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579909"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ビューアーの状態で変更が発生したかどうかを示します。 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>パラメーター

 _ulDir_
  
> [in]ビューアーで発生した変更とフォームの予想される応答に関する情報を提供するフラグのビットマスク。 次のフラグを設定できます。
    
VCSTATUS_CATEGORY 
  
> 別のカテゴリに次または前のメッセージがあります。 
    
VCSTATUS_INTERACTIVE 
  
> フォームにユーザー インターフェイスが表示されます。 このフラグを設定しない場合、フォームは、通常はユーザー インターフェイスが表示される動詞に応答しても、ユーザー インターフェイスの表示を抑制する必要があります。 
    
VCSTATUS_MODAL 
  
> フォームは、フォーム ビューアーに対してモーダルになる必要があります。 
    
VCSTATUS_NEXT 
  
> フォーム ビューアーに次のメッセージがあります。 
    
VCSTATUS_PREV 
  
> フォーム ビューアーに前のメッセージがあります。 
    
VCSTATUS_READONLY 
  
> 削除、送信、および移動操作は無効にする必要があります。 
    
VCSTATUS_UNREAD 
  
> フォーム ビューアーに次または前の未読メッセージがあります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が成功しました。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormAdviseSink::OnChange** メソッドを呼び出して、ビューアーの状態の変更についてフォームに通知します。 通常、変更は、ビューアー内の次VCSTATUS_NEXTまたはVCSTATUS_PREVIOUSメッセージの有無に基づいて、VCSTATUS_NEXT または VCSTATUS_PREVIOUS フラグを設定またはクリアするのみです。 したがって、フォーム オブジェクトは、サポートする次または以前のアクションを有効または無効にします。 
  
ビュー コンテキストのVCSTATUS_MODAL設定VCSTATUS_INTERACTIVE作成後は、ビュー コンテキストで変更できません。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

このメソッドの具体的な実装は、フォームの詳細に完全に依存します。 ほとんどのフォーム オブジェクトは、このメソッドを使用してユーザー インターフェイスを変更します (たとえば、ビューアーの状態フラグ パラメーターに一致するメニュー コマンドやボタンを有効または無効にします)。
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

