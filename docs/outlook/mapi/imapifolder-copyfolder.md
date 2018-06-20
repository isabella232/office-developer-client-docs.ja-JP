---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5961e7a2118a46bdc9c0e66138363976ae2f7154
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800477"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**適用されます**: Outlook 
  
サブフォルダーを移動またはコピーします。
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]サブフォルダーをコピーまたは移動するには、エントリの識別子へのポインター。
    
 _lpInterface_
  
> [in]_LpDestFolder_パラメーターが指すフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 フォルダーの標準的なインターフェイスを取得するサービス プロバイダーは、NULL を渡す[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。 に対する、IID_IMAPIProp、IID_IMAPIContainer、IID_IMAPIFolder、 _lpInterface_の有効な値が含まれます。 
    
 _lpDestFolder_
  
> [in]開いているフォルダーにコピーまたは移動したサブフォルダーが表示されるへのポインター。
    
 _lpszNewFolderName_
  
> [in]その新しい場所にコピーまたは移動したフォルダーの名前へのポインター。 _LpszNewFolderName_は、NULL に設定されている場合、コピー先のフォルダーの名前の複製元のサブフォルダーの名前が使用されます。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_に FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
COPY_SUBFOLDERS 
  
> すべてのサブフォルダーにコピーされるサブフォルダーにもコピーしてください。 コピー操作の COPY_SUBFOLDERS が設定されていない、 _lpEntryID_で識別されるサブフォルダーのみがコピーされます。 移動操作で、COPY_SUBFOLDERS の動作は既定のフラグが設定されているかどうかに関係なくです。 
    
FOLDER_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
FOLDER_MOVE 
  
> 代わりに移動するのには、サブフォルダーをコピーします。 FOLDER_MOVE が設定されていない場合は、サブフォルダーがコピーされます。
    
MAPI_DECLINE_OK 
  
> **CopyFolder**メソッドのサポート オブジェクトの[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)または[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)メソッドを呼び出すことによって実装されている場合は、 **CopyFolder**する必要があります代わりにすぐに返すこと MAPI_E_、メッセージ ストア プロバイダーの通知します。DECLINE_COPY。 
    
MAPI_UNICODE 
  
> Unicode 形式では、コピー先のフォルダーの名前です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフォルダー名です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 指定されたフォルダーは正常にコピーまたは移動されています。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定されたメッセージ ストア プロバイダーは、Unicode をサポートしていないまたは MAPI_UNICODE が設定されていないとメッセージ ストア プロバイダーは、Unicode だけをサポートしています。
    
MAPI_E_COLLISION 
  
> 移動またはコピーされているフォルダーの名前は、コピー先のフォルダーのサブフォルダーの名前と同じです。 メッセージ ストア プロバイダーには、一意のフォルダー名が必要です。
    
MAPI_E_DECLINE_COPY 
  
> プロバイダーのサポートのオブジェクトのメソッドを呼び出すことによってこのメソッドを実装して、呼び出し元に MAPI_DECLINE_OK フラグが渡されます。
    
MAPI_E_FOLDER_CYCLE 
  
> ソースフォルダーには直接的または間接的にコピー先のフォルダーが含まれています。 作業時間の大幅な可能性がありますが完了前に、この条件が検出された、元とコピー先のフォルダーを部分的に変更された可能性がありますので。 
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しが成功したが、すべてのエントリが正常にコピーされました。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

**IMAPIFolder::CopyFolder**メソッドは、コピーまたはサブフォルダーを別の場所に移動します。 サブフォルダーのコピーや移動は、サブフォルダーとして、コピー先のフォルダーに追加されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

コピーまたは移動操作には、COPY_SUBFOLDERS フラグを設定することによって示されているように、複数のフォルダーが含まれている場合、可能な限り完全にフォルダーごとに操作を実行します。 移動またはコピーするフォルダーのいずれかの場合があります存在しないまたは既に移動または別の場所にコピーします。 メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。
  
コピーしたメッセージですべてのメッセージ エントリの識別子を保持しようとしてください。 エントリの識別子を保持するためにも実行してくださいする必要がありますが、必須ではありません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

次の条件下で、これらの戻り値を期待してください。
  
|**条件**|**戻り値**|
|:-----|:-----|
|**CopyFolder**が正常にコピーまたは、すべてのメッセージとサブフォルダーを移動します。  <br/> |S_OK  <br/> |
|**CopyFolder**は、正常にコピーまたはすべてのメッセージとサブフォルダーに移動できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**CopyFolder**は完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くエラー値  <br/> |
   
**CopyFolder**が完了することではない場合と仮定しないでその作業は実行されませんでした。 **CopyFolder**をコピーまたはエラーが発生する前に 1 つまたは複数のメッセージとサブフォルダーを移動することがされている可能性があります。 
  
_LpEntryID_で存在しないフォルダーのエントリ id が渡された場合に、 **CopyFolder**は、メッセージ ストアの実装によって MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。 
  
によって、メッセージ ストア プロバイダーでは、元のメッセージのエントリ id は、コピーされたメッセージには保持されない場合があります。 可能な限り、エントリの識別子を保持する必要がありますが、必須ではありません。 一般に次のシナリオに依存します。
  
- 2 種類のメッセージ ・ ストア間でフォルダーを移動するときを変更するエントリの識別子が保証されます。
    
- 同じ種類の 2 つのメッセージ ストア間でフォルダーを移動するときにほとんどのエントリ id を変更します。
    
- 同じメッセージ ・ ストア内の別の場所にフォルダーを移動すると、エントリの識別子または可能性がありますしない変更、メッセージによって、プロバイダーを格納します。
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnPasteFolder  <br/> |MFCMAPI では、1 つの場所からフォルダーをコピーするのにには、 **IMAPIFolder::CopyFolder**メソッドを使用します。 MFCMAPI では、コピー操作中に元のフォルダーを記憶して、実際に貼り付けの操作中にコピーを実行します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

