---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5cb92a74e20cddc9a7e86555980d6babdea7b32d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576052"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上のメッセージをコピーまたは移動します。
  
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
  
> [in]コピーまたは移動するメッセージを識別する [ENTRYLIST](entrylist.md) 構造体の配列へのポインター。 
    
 _lpInterface_
  
> [in]  _lpDestFolder_ パラメーターが指す移動先フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡した場合、サービス プロバイダーは標準のフォルダー インターフェイス [IMAPIFolder : IMAPIContainer を返します](imapifolderimapicontainer.md)。 クライアントは NULL を渡す必要があります。 他の呼び出し元は  _、lpInterface_ パラメーターを、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、またはIID_IMAPIFolder。 
    
 _lpDestFolder_
  
> [in]コピーまたは移動されたメッセージを受信する開いているフォルダーへのポインター。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは、クライアントが _ulFlags_ パラメーターに MESSAGE_DIALOG フラグを設定し _、lpProgress_ パラメーターに NULL を渡す場合を無視します。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DECLINE_OK 
  
> サポート オブジェクトの [IMAPISupport::D oCopyTo](imapisupport-docopyto.md)または [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md)メソッドを呼び出して **、IMAPIFolder::CopyMessages** を実装している場合は、メッセージ ストア プロバイダーに直ちに MAPI_E_DECLINE_COPY を返す通知を行います。 
    
MESSAGE_DIALOG 
  
> 操作が進むにつれて進行状況インジケーターが表示されます。
    
MESSAGE_MOVE 
  
> メッセージまたはメッセージは、コピーの代わりに移動されます。 このMESSAGE_MOVE設定されていない場合は、メッセージがコピーされます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージまたはメッセージが正常にコピーまたは移動されました。
    
MAPI_E_DECLINE_COPY 
  
> プロバイダーは、サポート オブジェクト メソッドを呼び出してこのメソッドを実装し、呼び出し元が MAPI_DECLINE_OK渡しました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常にコピーまたは移動されたという訳ではありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::CopyMessages メソッドは**、メッセージを別のフォルダーにコピーまたは移動します。 
  
読み取り/書き込み権限で開いたメッセージは、移動またはコピーできます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

[IMAPISupport::CopyMessages](imapisupport-copymessages.md)メソッドを使用せずに別のメッセージ ストアにメッセージをコピーする場合は、最初に[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を GENERATE_RECEIPT_ONLY フラグ セットで呼び出す必要があります。 受信メッセージ ストアは、コピーまたは移動されたメッセージの読み取りレポートを生成する責任を負いません。 **IMAPISupport::CopyMessages** を呼び出して **IMAPIFolder::CopyMessages** を実装する場合は **、SetReadFlags を呼び出さない**。MAPI が呼び出します。 
  
実装では、メッセージを任意の順序で移動またはコピーし、任意の順序で読み取り状態レポートを生成できます。 つまり、メッセージのコピーを完了してから、読み取り状態レポートを生成するか、または実装がコピー操作を開始する前にレポートを送信できます。 ただし、コピーが成功したかどうかに関係なく、すべてのメッセージをコピーするために読み取りレポートを送信する必要があります。
  
コピー操作または移動操作に複数のメッセージが含まれる場合は、可能な限り完全に操作を実行します。 メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。
  
移動操作またはコピー操作全体でエントリ識別子を維持してみてください。 必須ではないが、エントリ識別子も保持する必要があります。
  
メッセージを移動またはコピーするときに通知を送信し、クライアントがメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドへの呼び出しが失敗する可能性があります。 
  
コピーまたは移動操作にメッセージの状態を含めない。 メッセージの状態を移動またはコピーすると、パフォーマンスに大きな影響を与えます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**IMAPIFolder::CopyMessages** を使用して検索結果フォルダーを作成します。メッセージは多くの場合、親フォルダーでグループ化されます。 
  
これらの戻り値は、次の条件下で期待してください。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages は** 、すべてのメッセージを正常にコピーまたは移動しました。  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** は、すべてのメッセージを正常にコピーまたは移動できなかった。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** を完了できません。  <br/> |エラー値  <br/> |
   
**IMAPIFolder::CopyMessages** を完了できない場合は、作業が完了していないと想定しません。 **IMAPIFolder::CopyMessages は** 、エラーが発生する前に 1 つ以上のメッセージをコピーまたは移動できた可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

