---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 65c9727a2af44a939263342dfca01ac7b9c128ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630825"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サブフォルダーをコピーまたは移動します。
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]コピーまたは移動するサブフォルダーのエントリ識別子へのポインター。
    
 _lpInterface_
  
> [in]  _lpDestFolder_ パラメーターが指すフォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、サービス プロバイダーは標準のフォルダー インターフェイス [IMAPIFolder : IMAPIContainer を返します](imapifolderimapicontainer.md)。 _lpInterface_ の有効な値には、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、およびIID_IMAPIFolder。 
    
 _lpDestFolder_
  
> [in]コピーまたは移動されたサブフォルダーを受け取る開いているフォルダーへのポインター。
    
 _lpszNewFolderName_
  
> [in]コピーまたは移動したフォルダーの新しい移動先の名前へのポインター。 _lpszNewFolderName_ が NULL に設定されている場合は、移動先フォルダーの名前にソース サブフォルダーの名前が使用されます。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で FOLDER_DIALOGフラグが設定されていない限り無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
COPY_SUBFOLDERS 
  
> コピーするサブフォルダー内のすべてのサブフォルダーもコピーする必要があります。 コピー COPY_SUBFOLDERS設定されていない場合は  _、lpEntryID_ で識別されるサブフォルダーだけがコピーされます。 移動操作では、フラグCOPY_SUBFOLDERSに関係なく、既定の動作になります。 
    
FOLDER_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
FOLDER_MOVE 
  
> サブフォルダーはコピーの代わりに移動されます。 このFOLDER_MOVE設定されていない場合、サブフォルダーがコピーされます。
    
MAPI_DECLINE_OK 
  
> メッセージ ストア プロバイダーに、サポート オブジェクトの [IMAPISupport::D oCopyTo](imapisupport-docopyto.md)または [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md)メソッドを呼び出して **CopyFolder** を実装する場合 **、CopyFolder** は直ちに MAPI_E_DECLINE_COPY を返す必要があります。 
    
MAPI_UNICODE 
  
> 移動先フォルダーの名前は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、フォルダー名は ANSI 形式です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したフォルダーが正常にコピーまたは移動されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定され、メッセージ ストア プロバイダーが Unicode をサポートしていないか、または MAPI_UNICODEが設定されていないと、メッセージ ストア プロバイダーは Unicode のみをサポートします。
    
MAPI_E_COLLISION 
  
> 移動またはコピーされるフォルダーの名前は、移動先フォルダー内のサブフォルダーの名前と同じです。 メッセージ ストア プロバイダーには、一意のフォルダー名が必要です。
    
MAPI_E_DECLINE_COPY 
  
> プロバイダーは、サポート オブジェクト メソッドを呼び出してこのメソッドを実装し、呼び出し元が MAPI_DECLINE_OK渡しました。
    
MAPI_E_FOLDER_CYCLE 
  
> ソース フォルダーには、直接または間接的に移動先フォルダーが含まれる。 この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース フォルダーと移動先フォルダーが部分的に変更される可能性があります。 
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常にコピーされたという訳ではありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::CopyFolder** メソッドは、サブフォルダーをある場所から別の場所にコピーまたは移動します。 コピーまたは移動するサブフォルダーは、サブフォルダーとして移動先フォルダーに追加されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

COPY_SUBFOLDERS フラグを設定することで示されている、コピーまたは移動操作に複数のフォルダーが含まれる場合は、フォルダーごとに可能な限り完全に操作を実行します。 移動またはコピーするフォルダーの 1 つが存在しない場合や、既に他の場所に移動またはコピーされている場合があります。 メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。
  
コピーされたメッセージ内のすべてのメッセージ エントリ識別子を保持してみてください。 また、エントリ識別子を保持する必要がありますが、必須ではありません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件下で期待してください。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**CopyFolder は** 、すべてのメッセージとサブフォルダーを正常にコピーまたは移動しました。  <br/> |S_OK  <br/> |
|**CopyFolder は** 、すべてのメッセージとサブフォルダーを正常にコピーまたは移動できなかった。  <br/> |MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND  <br/> |
|**CopyFolder** を完了できません。  <br/> |エラー以外のエラー MAPI_E_NOT_FOUND  <br/> |
   
**CopyFolder を** 完了できない場合は、作業が完了していないと想定しません。 **エラーが発生する前に、CopyFolder** で 1 つ以上のメッセージとサブフォルダーをコピーまたは移動できた可能性があります。 
  
存在しないフォルダーのエントリ識別子が  _lpEntryID_ で渡された場合 **、CopyFolder** はメッセージ ストアの実装に応じて MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。 
  
メッセージ ストア プロバイダーによっては、元のメッセージのエントリ識別子がコピーされたメッセージに保持される場合と保存されない場合があります。 可能な限りエントリ識別子を保持する必要がありますが、要件ではありません。 通常、次のシナリオに依存できます。
  
- 2 つの異なる種類のメッセージ ストア間でフォルダーを移動すると、エントリ識別子が変更される保証があります。
    
- 同じ種類の 2 つのメッセージ ストア間でフォルダーを移動すると、エントリ識別子はほとんど常に変更されます。
    
- フォルダーを同じメッセージ ストア内の別の場所に移動すると、メッセージ ストア プロバイダーによっては、エントリ識別子が変更される場合と変更されない場合があります。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI は **IMAPIFolder::CopyFolder** メソッドを使用して、フォルダーをある場所から別の場所にコピーします。 MFCMAPI は、コピー操作中にソース フォルダーを記憶し、貼り付け操作中に実際にコピーを実行します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

