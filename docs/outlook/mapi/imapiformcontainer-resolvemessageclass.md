---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408552"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージクラスをフォームコンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>パラメーター

 _szmessageclass_
  
> 順番解決されるメッセージクラスの名前を示す文字列。 メッセージクラス名は常に ANSI 文字列で、Unicode はありません。
    
 _ulFlags_
  
> 順番メッセージクラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全一致のメッセージクラス文字列のみを解決する必要があります。
    
 _ppforminfo_
  
> 読み上げ返されるフォーム情報オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _szmessageclass_パラメーターで渡されたメッセージクラスが、フォームコンテナー内のフォームのメッセージクラスと一致しません。 
    
## <a name="remarks"></a>注釈

クライアントアプリケーションは、 **imapiformcontainer:: ResolveMessageClass**メソッドを呼び出して、form コンテナー内のフォームにメッセージクラスを解決します。 _ppforminfo_パラメーターで返されたフォーム情報オブジェクトは、指定されたメッセージクラスを使用して、フォームのプロパティにさらにアクセスできるようにします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージクラスをフォームに解決するには、解決するメッセージクラスの名前を渡します (例: `IPM.HelpDesk.Software`)。 解決策を正確にする (つまり、メッセージクラスの基本クラスに解決されないようにする) には、 _ulflags_パラメーターに MAPIFORM_EXACTMATCH フラグを渡すことができます。 
  
解決されたメッセージクラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。 [imapiformmgr::P repareform](imapiformmgr-prepareform.md)または[imapiformmgr:: CreateForm](imapiformmgr-createform.md)メソッドのいずれかを呼び出すまで、クラス識別子が OLE ライブラリに存在することを前提としていません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg  <br/> |CFormContainerDlg:: OnResolveMessageClass  <br/> |mfcmapi は、 **imapiformcontainer:: ResolveMessageClass**メソッドを使用して、メッセージクラスに関連付けられているフォームを特定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

