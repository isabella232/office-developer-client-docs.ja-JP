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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321610"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
form コンテナー内のフォームに対してメッセージクラスを解決し、そのフォームのフォーム情報オブジェクトを返します。
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>パラメーター

 _szmsgclass_
  
> 順番解決されるメッセージクラスの名前を示す文字列。
    
 _ulFlags_
  
> 順番メッセージクラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全一致のメッセージクラス文字列のみを解決する必要があります。
    
 _pfolderfocus_
  
> 順番解決されるメッセージを含むフォルダーへのポインター。 _pfolderfocus_パラメーターは NULL にすることができます。 
    
 _ppResult_
  
> 読み上げ返されるフォーム情報オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _szmsgclass_パラメーターで渡されたメッセージクラスが、フォームライブラリ内のフォームのメッセージクラスと一致しません。 
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiformmgr:: ResolveMessageClass**メソッドを呼び出して、form コンテナー内のフォームにメッセージクラスを解決します。 _ppResult_パラメーターで返されるフォーム情報オブジェクトは、指定されたメッセージクラスを持つフォームのプロパティへのアクセスをさらに提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージクラスをフォームに解決するために、フォームビューアーは解決するメッセージクラスの名前 (" `IPM.HelpDesk.Software`" など) を渡します。 解像度を正確にする (つまり、正確に一致するフォームサーバーが使用できない場合にメッセージクラスの基本クラスに解決されないようにする) には、 _ulflags_パラメーターに MAPIFORM_EXACTMATCH フラグを渡すことができます。 _pfolderfocus_パラメーターが NULL の場合、メッセージクラスの解決処理ではフォルダーコンテナーは検索されません。 
  
検索されるコンテナーの順序は、フォームライブラリプロバイダーの実装によって異なります。 既定のフォームライブラリプロバイダーは、最初にローカルコンテナーを検索し、次に、渡されたフォルダーのフォルダーコンテナー、個人用フォームコンテナー、そして組織コンテナーを検索します。
  
メッセージクラス名は常に ANSI 文字列で、Unicode はありません。
  
解決されたメッセージクラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。 フォームビューアーが OLE ライブラリ内に存在することを前提としているのは、フォームビューアーが[imapiformmgr::P repareform](imapiformmgr-prepareform.md)メソッドまたは[imapiformmgr:: CreateForm](imapiformmgr-createform.md)メソッドを呼び出したときまでです。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

