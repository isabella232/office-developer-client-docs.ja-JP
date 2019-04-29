---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436763"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいサブフォルダーを作成します。
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a>パラメーター

 _ulfoldertype_
  
> 順番作成するフォルダーの種類を示します。 次のフラグを設定できます。
    
FOLDER_GENERIC 
  
> 汎用フォルダーを作成する必要があります。
    
FOLDER_SEARCH 
  
> 検索結果フォルダーを作成する必要があります。
    
 _lpszfoldername_
  
> 順番新しいフォルダーの名前を含む文字列へのポインター。 この名前は、新しいフォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの基礎となります。
    
 _lpszfoldercomment_
  
> 順番新しいフォルダーに関連付けられているコメントを含む文字列へのポインター。 この文字列は、新しいフォルダーの**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) プロパティの値になります。 NULL が渡された場合、フォルダーには最初のコメントがありません。
    
 _lpinterface_
  
> 順番新しいフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、メッセージストアプロバイダーは標準のフォルダーインターフェイス、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)を返します。 クライアントは、NULL を渡す必要があります。 他の呼び出し元が_lpinterface_パラメーターを IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder に設定できます。 
    
 _ulFlags_
  
> 順番フォルダーの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元クライアントが新しいフォルダーを完全に使用できるようになるまで、 **CreateFolder**が正常に戻ることができるようにします。 新しいフォルダーを使用できない場合は、それ以降の呼び出しを行うとエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> フォルダーの名前は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、フォルダー名は ANSI 形式になります。
    
OPEN_IF_EXISTS 
  
> 指定した名前の既存のフォルダーを開いて、 _lpszfoldername_パラメーターで指定されたフォルダーが既に存在する場合でも、メソッドを正常に実行できるようにします。 兄弟フォルダーに同じ名前を付けることができるメッセージストアプロバイダーは、指定された名前で複数のフォルダーが存在する場合は、既存のフォルダーを開かないことに注意してください。 
    
 _lppfolder_
  
> 読み上げ新しく作成されたフォルダーへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> OPEN_IF_EXISTS フラグが設定されている場合、新しいフォルダーが正常に作成または開きます。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_COLLISION 
  
> _lpszfoldername_パラメーターに指定した名前のフォルダーが既に存在します。 フォルダー名は一意である必要があります。 
    
## <a name="remarks"></a>注釈

**imapifolder:: CreateFolder**メソッドを実行すると、現在のフォルダーにサブフォルダーが作成され、新しいフォルダーにエントリ識別子が割り当てられます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateFolder**が返された場合は、新しいフォルダーのエントリ識別子が使用できない可能性があることに注意してください。 メッセージストアプロバイダーによっては、完全に保存するために、新しいフォルダーの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後に、エントリ識別子を使用できないことがあります。 これは、MAPI_DEFERRED_ERRORS フラグが設定されている場合に特に当てはまります。 
  
一部のメッセージストアプロバイダーは、 _lpinterface_パラメーターに渡す値に関係なく、常に_lppfolder_パラメーターをフォルダーの標準インターフェイスにポイントすることに注意してください。 返されるインターフェイスポインターが予期した型ではない場合があるため、新しいフォルダーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティを取得します。 必要に応じて、他の呼び出しを行う前に、適切な型にポインターをキャストしてください。
  
ほとんどのメッセージストアプロバイダーでは、兄弟フォルダーの名前に対して一意の新しいフォルダー名が必要です。 このルールに従っていない場合に返される MAPI_E_COLLISION エラー値を処理できるようにします。 
  
新しく作成されたフォルダーのエントリ識別子を特定するには、新しいフォルダーの**imapiprop:: GetProps**メソッドを呼び出して、そのフォルダーの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを取得します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg  <br/> |CMsgStoreDlg:: OnCreateSubFolder  <br/> |mfcmapi は、 **CMsgStoreDlg:: OnCreateSubFolder**メソッドを使用して、mfcmapi に新しいフォルダーを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

