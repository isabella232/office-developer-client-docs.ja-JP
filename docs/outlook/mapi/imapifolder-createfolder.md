---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 41590cc2968c919afac714c348beda8a653f81ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610651"
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

 _ulFolderType_
  
> [in]作成するフォルダーの種類。 次のフラグを設定できます。
    
FOLDER_GENERIC 
  
> 汎用フォルダーを作成する必要があります。
    
FOLDER_SEARCH 
  
> 検索結果フォルダーを作成する必要があります。
    
 _lpszFolderName_
  
> [in]新しいフォルダーの名前を含む文字列へのポインター。 この名前は、新しいフォルダーのプロパティ [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)**プロパティPR_DISPLAY_NAME基** になります。
    
 _lpszFolderComment_
  
> [in]新しいフォルダーに関連付けられたコメントを含む文字列へのポインター。 この文字列は、新しいフォルダーのプロパティ ([PidTagComment](pidtagcomment-canonical-property.md)) **PR_COMMENT** の値になります。 NULL が渡された場合、フォルダーには最初のコメントはありません。
    
 _lpInterface_
  
> [in]新しいフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、メッセージ ストア プロバイダーは標準のフォルダー インターフェイス [IMAPIFolder : IMAPIContainer を返します](imapifolderimapicontainer.md)。 クライアントは NULL を渡す必要があります。 他の呼び出し元は  _、lpInterface_ パラメーターを、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、またはIID_IMAPIFolder。 
    
 _ulFlags_
  
> [in]フォルダーの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 新しいフォルダーが呼び出し元のクライアントで完全に使用できる前に **、CreateFolder** を正常に返します。 新しいフォルダーを使用できない場合は、そのフォルダーを後続の呼び出しで呼び出した場合、エラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> フォルダーの名前は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、フォルダー名は ANSI 形式です。
    
OPEN_IF_EXISTS 
  
> _lpszFolderName_ パラメーターで指定されたフォルダーが既に存在する場合でも、その名前を持つ既存のフォルダーを開いて、メソッドを成功できます。 同じ名前の兄弟フォルダーを許可するメッセージ ストア プロバイダーは、指定された名前で複数のフォルダーが存在する場合、既存のフォルダーを開かない場合があります。 
    
 _lppFolder_
  
> [out]新しく作成されたフォルダーへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 新しいフォルダーが正常に作成または開かされました (OPEN_IF_EXISTSが設定されている場合)。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_COLLISION 
  
> _lpszFolderName_ パラメーターに指定された名前を持つフォルダーが既に存在します。 フォルダー名は一意である必要があります。 
    
## <a name="remarks"></a>注釈

**IMAPIFolder::CreateFolder** メソッドは、現在のフォルダーにサブフォルダーを作成し、新しいフォルダーにエントリ識別子を割り当てる。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateFolder が返** される場合は、新しいフォルダーのエントリ識別子が使用できない可能性があります。 一部のメッセージ ストア プロバイダーは、新しいフォルダーの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出して完全に保存するまで、エントリ識別子を使用できません。 これは、このフラグを設定している場合は特にMAPI_DEFERRED_ERRORSです。 
  
一部のメッセージ ストア プロバイダーは _、lpInterface_ パラメーターに渡す値に関係なく、常に _lppFolder_ パラメーターをフォルダーの標準インターフェイスにポイントします。 返されるインターフェイス ポインターは、必要な種類ではない可能性があります。ため、新しいフォルダーの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して **、PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティを取得します。 必要に応じて、他の呼び出しを行う前に、ポインターをより適切な型にキャストします。
  
ほとんどのメッセージ ストア プロバイダーでは、新しいフォルダーの名前が兄弟フォルダーの名前に対して一意である必要があります。 このルールに従MAPI_E_COLLISION返されるエラー値を処理できます。 
  
新しく作成したフォルダーのエントリ識別子を確認するには、新しいフォルダーの **IMAPIProp::GetProps** メソッドを呼び出して、PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを取得します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI は **、CMsgStoreDlg::OnCreateSubFolder** メソッドを使用して、MFCMAPI で新しいフォルダーを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

