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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 36fd729b1ca3e5d877d03358d581b83fc6d4782c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800484"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _ulFolderType_
  
> [in]作成するフォルダーの種類。 次のフラグを設定することができます。
    
FOLDER_GENERIC 
  
> 汎用フォルダーを作成する必要があります。
    
FOLDER_SEARCH 
  
> 検索結果のフォルダーを作成する必要があります。
    
 _lpszFolderName_
  
> [in]新しいフォルダーの名前を含む文字列へのポインター。 この名前は、新しいフォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティの基本です。
    
 _lpszFolderComment_
  
> [in]新しいフォルダーに関連付けられているコメントを含む文字列へのポインター。 この文字列では、新しいフォルダーの**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) のプロパティの値になります。 NULL を渡した場合、フォルダーの初期のコメントはありません。
    
 _lpInterface_
  
> [in]新しいフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 メッセージ ストア プロバイダーは、フォルダーの標準的なインタ フェースを取得すると、NULL を渡す[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。 クライアントでは、NULL を渡す必要があります。 他の呼び出し元に対する、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder、 _lpInterface_パラメーターを設定できます。 
    
 _ulFlags_
  
> [in]フォルダーを作成する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> **CreateFolder**を正常に戻す、可能性のある新しいフォルダーは、呼び出し側のクライアントに完全に利用できる前にするにを使用できます。 新しいフォルダーが使用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。 
    
MAPI_UNICODE 
  
> フォルダーの名前は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフォルダー名です。
    
OPEN_IF_EXISTS 
  
> により、その名前を持つ既存のフォルダーを開いて、既に_lpszFolderName_パラメーターで指定されたフォルダーが存在する場合でも成功します。 メッセージ ストア プロバイダーの兄弟に同じ名前のフォルダーを開けない可能性があります既存のフォルダーは、指定された名前の 1 つ以上存在する場合に注意してください。 
    
 _lppFolder_
  
> [out]新しく作成したフォルダーへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 新しいフォルダーが正常に作成または開くと、OPEN_IF_EXISTS フラグが設定されている場合。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_COLLISION 
  
> 既に、 _lpszFolderName_パラメーターで指定された名前を持つフォルダーが存在します。 フォルダー名は一意である必要があります。 
    
## <a name="remarks"></a>備考

**IMAPIFolder::CreateFolder**メソッドは現在のフォルダーにサブフォルダーを作成し、新しいフォルダーのエントリ id を割り当てます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateFolder**が返される場合、その新しいフォルダーのエントリ id が使用できない可能性があります。 メッセージ ストアのプロバイダーによっては行わないでくださいエントリ id まで使用可能な恒久的に保存するための新しいフォルダーの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後。 これは、MAPI_DEFERRED_ERRORS フラグを設定している場合に特に当てはまります。 
  
メッセージ ストアのプロバイダーによっては、フォルダーの標準的なインタ フェースに、 _lpInterface_パラメーターに渡す値に関係なく、 _lppFolder_パラメーターを常にポイントに注意します。 返されるインターフェイス ポインターは、必要な種類のできない場合があります、ためには、 **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティを取得するために新しいフォルダーの[IMAPIProp::GetProps](imapiprop-getprops.md)のメソッドを呼び出します。 必要に応じて、他の呼び出しを行う前より適切な型へのポインターをキャストします。
  
通常メッセージ ストア プロバイダーでは、その兄弟フォルダー名に対して一意にする新しいフォルダーの名前が必要です。 この規則に従わない場合に、MAPI_E_COLLISION エラー値を処理できるようにするには。 
  
新しく作成したフォルダーのエントリ id を確認するのに、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを取得するために、新しいフォルダーの**IMAPIProp::GetProps**メソッドを呼び出します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI では、 **CMsgStoreDlg::OnCreateSubFolder**メソッドを使用して、MFCMAPI で新しいフォルダーを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

