---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3567a0bc4c24ecdeefe6d58fe0075b1979001407
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561517"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPISession::ShowForm](imapisession-showform.md)メソッドがメッセージにアクセスするために使用する数値トークンを作成します。 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 **null を渡** す場合、標準インターフェイス [(IMessage)](imessageimapiprop.md)が使用されます。 _lpInterface パラメーターは_ null または **IID_IMessage。** 
    
 _lpMessage_
  
> [in]フォームに表示するメッセージへのポインター。
    
 _lpulMessageToken_
  
> [out]メッセージ トークンへのポインター。 **これは、IMAPISession::ShowForm** メソッドが  _lpMessage_ で指すメッセージにアクセスするために使用されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームの準備が成功しました。
    
## <a name="remarks"></a>注釈

**IMAPISession::P repareForm** メソッドは _、lpMessage_ パラメーターが指すメッセージのメッセージ トークンを作成し、メッセージの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 このトークンは  _ulMessageToken_ パラメーターで **IMAPISession::ShowForm に渡されます**。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareForm** の呼び出しが成功した場合は **、ShowForm** を呼び出す前に [、その IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して _lpMessage_ が指すメッセージを解放します。 ShowForm を呼び出す前にメッセージを解放 **すると、** メモリ リークが発生する可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI は **IMAPISession::P repareForm** メソッドを **IMAPISession::ShowForm** と共に使用して、モーダル フォームでメッセージを表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

