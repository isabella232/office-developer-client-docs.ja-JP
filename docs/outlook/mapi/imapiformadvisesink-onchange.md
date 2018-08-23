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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e32157f41632b782fbacf87e0411c18d167b4279
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576681"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム ビューアーのステータスに変更が発生したことを示します。 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>パラメーター

 _ulDir_
  
> [in]ビューアーと、フォーム内の予想される応答で発生した変更に関する情報を提供するフラグのビットマスクです。 次のフラグを設定することができます。
    
VCSTATUS_CATEGORY 
  
> 別のカテゴリで次または前のメッセージが表示されます。 
    
VCSTATUS_INTERACTIVE 
  
> フォームは、ユーザー インターフェイスを表示する必要があります。 このフラグが設定されていない場合、フォームが動詞が表示されるユーザー インターフェイスは、通常原因への応答であっても、ユーザー インターフェイスを表示するを抑制する必要があります。 
    
VCSTATUS_MODAL 
  
> フォームがモーダル フォーム ビューアーに表示します。 
    
VCSTATUS_NEXT 
  
> フォーム ビューアーに次のメッセージが表示されます。 
    
VCSTATUS_PREV 
  
> フォーム ビューアーで前のメッセージが表示されます。 
    
VCSTATUS_READONLY 
  
> 削除、送信、および移動の操作を無効にする必要があります。 
    
VCSTATUS_UNREAD 
  
> フォーム ビューアーで次または前の未読メ ッ セージがあります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が正常に完了しました。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは、ビューアーのステータスの変更のフォームを通知するために**IMAPIFormAdviseSink::OnChange**メソッドを呼び出します。 通常、唯一の変更は設定か、ビューアー内の次または前のメッセージの有無に基づいて、VCSTATUS_NEXT または VCSTATUS_PREVIOUS フラグをオフにします。 したがって、フォーム オブジェクトは、有効または、サポートする前または次のアクションを無効にします。 
  
VCSTATUS_MODAL と VCSTATUS_INTERACTIVE の設定は、それが作成された後、ビューのコンテキストで変更できません。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

このメソッドの特定の実装では、フォームの仕様に完全に依存しています。 フォームのほとんどのオブジェクトは、独自のユーザー インターフェイス (たとえば、有効にするか、ビューアーのステータス フラグのパラメーターと一致するのにには、メニュー コマンドやボタンを無効にするのに場合など) を変更するのにはこのメソッドを使用します。
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

