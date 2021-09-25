---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8ea8a07c8b299c254fbbb8fd914838c916c5684f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596209"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>パラメーター

 _szMsgClass_
  
> [in]解決されるメッセージ クラスの名前を示す文字列。
    
 _ulFlags_
  
> [in]メッセージ クラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラスの文字列のみを解決する必要があります。
    
 _pFolderFocus_
  
> [in]解決するメッセージを含むフォルダーへのポインター。 _pFolderFocus パラメーター_ には NULL を指定できます。 
    
 _ppResult_
  
> [out]返されるフォーム情報オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _szMsgClass_ パラメーターで渡されたメッセージ クラスは、フォーム ライブラリ内のフォームのメッセージ クラスと一致しません。 
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::ResolveMessageClass** メソッドを呼び出して、フォーム コンテナー内のフォームにメッセージ クラスを解決します。 _ppResult_ パラメーターで返されるフォーム情報オブジェクトは、指定されたメッセージ クラスを持つフォームのプロパティにさらにアクセスできます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ クラスをフォームに解決するために、フォーム ビューアーは解決するメッセージ クラスの名前 ("" など) を渡 `IPM.HelpDesk.Software` します。 解決を厳密に (つまり、完全に一致するフォーム サーバーが使用できない場合にメッセージ クラスの基本クラスの解決を防ぐため) には  _、ulFlags_ パラメーターに MAPIFORM_EXACTMATCH フラグを渡します。 _pFolderFocus パラメーター_ が NULL の場合、メッセージ クラス解決プロセスではフォルダー コンテナーは検索されません。 
  
検索されるコンテナーの順序は、フォーム ライブラリ プロバイダーの実装によって異なります。 既定のフォーム ライブラリ プロバイダーは、最初にローカル コンテナーを検索し、次にフォルダー コンテナーで、渡されたフォルダー、個人用フォーム コンテナー、最後に組織コンテナーを検索します。
  
メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。
  
解決されたメッセージ クラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。 フォーム ビューアーは、フォーム ビューアーが [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) メソッドまたは [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) メソッドのいずれかを呼び出すまで、OLE ライブラリにクラス識別子が存在することを前提として機能しません。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

