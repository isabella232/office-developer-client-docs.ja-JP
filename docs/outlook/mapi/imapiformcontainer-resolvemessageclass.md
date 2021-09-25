---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 43273b0f725b962a51a38009aab0bd5592c5644b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630804"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>パラメーター

 _szMessageClass_
  
> [in]解決されるメッセージ クラスの名前を示す文字列。 メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。
    
 _ulFlags_
  
> [in]メッセージ クラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラスの文字列のみを解決する必要があります。
    
 _ppforminfo_
  
> [out]返されるフォーム情報オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _szMessageClass_ パラメーターで渡されたメッセージ クラスは、フォーム コンテナー内のフォームのメッセージ クラスと一致しません。 
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは **IMAPIFormContainer::ResolveMessageClass** メソッドを呼び出して、フォーム コンテナー内のフォームにメッセージ クラスを解決します。 _ppforminfo_ パラメーターで返されるフォーム情報オブジェクトは、指定されたメッセージ クラスを使用してフォームのプロパティにさらにアクセスできます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ クラスをフォームに解決するには、解決するメッセージ クラスの名前を渡します (たとえば  `IPM.HelpDesk.Software` )。 解決を厳密に (つまり、メッセージ クラスの基本クラスへの解決を防ぐため) には  _、ulFlags_ パラメーターに MAPIFORM_EXACTMATCH フラグを渡します。 
  
解決されたメッセージ クラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。 [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md)メソッドまたは[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)メソッドのいずれかを呼び出すまで、OLE ライブラリにクラス識別子が存在することを想定しません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI は **IMAPIFormContainer::ResolveMessageClass** メソッドを使用して、メッセージ クラスに関連付けられているフォームを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

