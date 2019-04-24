---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335766"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[imapisession:: showform](imapisession-showform.md)メソッドがメッセージにアクセスするために使用する数値トークンを作成します。 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>パラメーター

 _lpinterface_
  
> 順番メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 標準インターフェイスまたは[IMessage](imessageimapiprop.md)で**null**結果が渡されています。 _lpinterface_パラメーターは、 **null**または IID_IMessage である必要があります。 
    
 _lpmessage_
  
> 順番フォームに表示されるメッセージへのポインター。
    
 _lアウト messagetoken_
  
> 読み上げ_lpmessage_によって参照されるメッセージにアクセスするために**imapisession:: showform**メソッドによって使用されるメッセージトークンへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームの準備が正常に完了しました。
    
## <a name="remarks"></a>解説

**imapisession::P repareform**メソッドは、 _lpmessage_パラメーターによって示されるメッセージのメッセージトークンを作成し、メッセージの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 このトークンは、 _ulmessagetoken_パラメーターで**imapisession:: showform**に渡されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareForm**の呼び出しが成功した場合は、 **showform**を呼び出す前に[IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して、 _lpmessage_に示されているメッセージを解放します。 **showform**を呼び出す前にメッセージを解放しないと、メモリリークが発生する可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions  <br/> |openmessagemodal  <br/> |mfcmapi は、imapisession: **:P repareform**メソッドを**imapisession:: showform**と共に使用して、モーダルフォームにメッセージを表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

