---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3cd84e4ddb6d722d9f3de11d65b100d86e69ecae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571816"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。
  
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
  
> [in]解決するメッセージ クラスの名前を示す文字列です。
    
 _ulFlags_
  
> [in]メッセージ クラスが解決される方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラス文字列のみを解決する必要があります。
    
 _pFolderFocus_
  
> [in]解決されているメッセージを含むフォルダーへのポインター。 _PFolderFocus_パラメーターは NULL にできます。 
    
 _ppResult_
  
> [out]返されたフォームの情報オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _SzMsgClass_パラメーターで渡されたメッセージ クラスでは、フォーム ライブラリ内の任意のフォームのメッセージ クラスが一致しません。 
    
## <a name="remarks"></a>注釈

フォームの閲覧者は、フォームのコンテナー内のフォームにメッセージ クラスを解決するのには**IMAPIFormMgr::ResolveMessageClass**メソッドを呼び出します。 _PpResult_パラメーターに返されるフォームの情報オブジェクトを特定のメッセージ クラスを含むフォームのプロパティへのアクセスをさらに提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォームにメッセージ クラスを解決する、フォーム ビューアーを渡すように、解決するメッセージ クラスの名前" `IPM.HelpDesk.Software`"です。 正確な解像度を強制する (つまりと正確に一致する、フォーム、のメッセージ クラスの基本クラスの解像度を防止するためにサーバーは使用できません)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。 _PFolderFocus_パラメーターが NULL の場合は、メッセージのクラスの解決プロセスは、フォルダー コンテナーを検索しません。 
  
検索コンテナーの順序は、フォーム ライブラリのプロバイダーの実装に依存します。 既定のフォーム ライブラリのプロバイダーは、ローカルのコンテナーでは、[フォルダーのコンテナー、渡されたフォルダー、個人用フォームのコンテナーと、最後に、[組織] コンテナーを最初に検索します。
  
メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。
  
フォームの情報オブジェクトの一部として解決済みのメッセージ クラスのクラス識別子が返されます。 フォーム ビューアー フォーム ビューアーは、 [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)メソッドまたは[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)メソッドが呼び出されるとするまで、OLE ライブラリのクラス識別子が存在することを前提として動作していません。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

