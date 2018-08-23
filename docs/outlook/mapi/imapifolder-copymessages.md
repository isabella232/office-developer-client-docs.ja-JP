---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e253aa6a701d565fbc61e8a0e0a6388f7199c000
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593264"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
1 つまたは複数のメッセージを移動またはコピーします。
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpMsgList_
  
> [in]メッセージまたはメッセージのコピーまたは移動を識別する[ENTRYLIST](entrylist.md)構造体の配列へのポインター。 
    
 _lpInterface_
  
> [in]_LpDestFolder_パラメーターで指定された移動先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 フォルダーの標準的なインターフェイスを返すサービス プロバイダーの結果をパラメーターに NULL [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。 クライアントでは、NULL を渡す必要があります。 他の呼び出し元に対する、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder、 _lpInterface_パラメーターを設定できます。 
    
 _lpDestFolder_
  
> [in]開いているフォルダーにコピーまたは移動されたメッセージを受信するへのポインター。
    
 _ulUIParam_
  
> [in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。 _UlUIParam_パラメーターは、クライアントは、 _ulFlags_パラメーターに MESSAGE_DIALOG フラグを設定し、 _lpProgress_パラメーターに NULL を渡す場合を除き、無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を実現する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DECLINE_OK 
  
> サポート オブジェクトの[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)または[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)メソッドを呼び出すことによって**IMAPIFolder::CopyMessages**を実装している場合に MAPI_E_DECLINE_COPY をすぐに返すメッセージ ストア プロバイダーに通知します。 
    
MESSAGE_DIALOG 
  
> 操作の進行中は、進行状況のインジケーターを表示します。
    
MESSAGE_MOVE 
  
> 代わりに移動するのには、メッセージまたはメッセージをコピーします。 MESSAGE_MOVE が設定されていない場合、メッセージがコピーされます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージまたはメッセージがされて正常にコピーまたは移動します。
    
MAPI_E_DECLINE_COPY 
  
> プロバイダーのサポートのオブジェクトのメソッドを呼び出すことによってこのメソッドを実装して、呼び出し元に MAPI_DECLINE_OK フラグが渡されます。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しが成功したが、すべてのエントリが正常にコピーまたは移動されました。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::CopyMessages**メソッドは、コピーまたは別のフォルダーにメッセージを移動します。 
  
開かれているメッセージ読み取り/書き込みアクセス許可を移動またはコピーすることができます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

[IMAPISupport::CopyMessages](imapisupport-copymessages.md)メソッドを使用せず、別のメッセージ ストアにメッセージをコピーする場合は、GENERATE_RECEIPT_ONLY フラグを設定して[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を最初に呼び出す必要があります。 受信側メッセージ ・ ストアは、コピーまたは移動されたメッセージの読み取りのレポートを生成するための責任ではありません。 場合は**IMAPIFolder::CopyMessages**を実装するために**IMAPISupport::CopyMessages**を呼び出す場合、呼び出さないように**SetReadFlags**。MAPI を呼び出すことです。 
  
実装は、移動または任意の順序でメッセージをコピーし、任意の順序で読み取りステータス レポートを生成できます。 読み取りステータス レポートを生成する前にメッセージのコピーを完了したり、実装は、コピー操作を開始する前にレポートを送信できます。 ただし、コピーが成功するかどうかに関係なく、コピーするすべてのメッセージを送信するレポートを読みます。
  
コピーまたは移動操作には、複数のメッセージが含まれている場合は、できるだけ完全に操作を実行します。 メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。
  
移動またはコピー操作の間でのエントリの識別子を維持しようとしてください。 必須ではありませんが、エントリの識別子を維持することもする必要があります。
  
移動またはクライアントがメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しは失敗する可能性があることあらかじめご了承するようにメッセージをコピーするときに通知を送信します。 
  
メッセージの状態は、コピー、移動の操作をしたりしないでください。 移動またはメッセージの状態のコピーを大幅にパフォーマンスに影響します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**IMAPIFolder::CopyMessages**を使用して、検索結果のフォルダー、メッセージ多くの場合、親フォルダー グループを作成します。 
  
次の条件下で、これらの戻り値を期待してください。
  
|**条件**|**戻り値**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages**が正常にコピーまたは、すべてのメッセージを移動します。  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages**は、正常にコピーまたはすべてのメッセージを移動できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages**は完了できませんでした。  <br/> |エラー値  <br/> |
   
**IMAPIFolder::CopyMessages**が完了することではない場合と仮定しないでその作業は実行されませんでした。 **IMAPIFolder::CopyMessages**は、コピーまたはエラーが発生する前に 1 つまたは複数のメッセージを移動することがされている可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

