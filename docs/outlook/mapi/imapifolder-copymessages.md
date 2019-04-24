---
title: imapifoldercopymessages
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
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280128"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数のメッセージをコピーまたは移動します。
  
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

 _lpmsglist_
  
> 順番コピーまたは移動するメッセージを識別する[entrylist](entrylist.md)構造体の配列へのポインター。 
    
 _lpinterface_
  
> 順番_lpdestfolder_パラメーターによって指定された宛先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 サービスプロバイダーに NULL 結果が渡され、標準のフォルダーインターフェイス、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)が返されます。 クライアントは、NULL を渡す必要があります。 他の呼び出し元が_lpinterface_パラメーターを IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder に設定できます。 
    
 _lpdestfolder_
  
> 順番コピーまたは移動されたメッセージを受信する、開いているフォルダーへのポインター。
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、クライアントが_ulflags_パラメーターに MESSAGE_DIALOG フラグを設定し、 _lpprogress_パラメーターに NULL を渡す場合を除き、無視されます。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
 _ulFlags_
  
> 順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DECLINE_OK 
  
> サポートオブジェクトの[imapifolder::D ocopyto](imapisupport-docopyto.md)または[imapifolder::D ocopyprops](imapisupport-docopyprops.md)メソッドを呼び出して、 **imapifolder:: copymessages**を実装することによって、メッセージストアプロバイダーに直ちに MAPI_E_DECLINE_COPY を返すように通知します。 
    
MESSAGE_DIALOG 
  
> 操作の進行状況を示すインジケーターを表示します。
    
MESSAGE_MOVE 
  
> メッセージをコピーではなく移動します。 MESSAGE_MOVE が設定されていない場合は、メッセージがコピーされます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージまたはメッセージが正常にコピーまたは移動されました。
    
MAPI_E_DECLINE_COPY 
  
> プロバイダーは、サポートオブジェクトのメソッドを呼び出すことによってこのメソッドを実装し、発信者が MAPI_DECLINE_OK フラグを渡しています。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常にコピーまたは移動されませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapifolder:: copymessages**メソッドは、メッセージを別のフォルダーにコピーまたは移動します。 
  
読み取り/書き込みアクセス許可を使用して開かれたメッセージは、移動またはコピーすることができます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

[imapisupport:: copymessages](imapisupport-copymessages.md)メソッドを使用せずにメッセージを別のメッセージストアにコピーする場合は、GENERATE_RECEIPT_ONLY フラグが設定された[imapisupport:: setreadflags](imapifolder-setreadflags.md)を最初に呼び出す必要があります。 受信側のメッセージストアは、コピーまたは移動されたメッセージの読み取りレポートを生成する責任がありません。 **imapisupport:** : copymessages を呼び出して**imapisupport:: copymessages**を実装する場合は、 **setreadflags**を呼び出さないでください。MAPI がこれを呼び出します。 
  
実装では、任意の順序でメッセージを移動またはコピーしたり、読み取り状態レポートを生成したりできます。 つまり、読み取り状態レポートを生成する前にメッセージのコピーを終了するか、または実装でコピー操作を開始する前にレポートを送信することができます。 ただし、コピーが成功したかどうかにかかわらず、すべてのメッセージをコピーするには、読み取りレポートを送信する必要があります。
  
コピー操作または移動操作に複数のメッセージが含まれている場合は、操作をできるだけ完全に実行します。 メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。
  
移動操作またはコピー操作の間にエントリ識別子を保持するようにしてください。 エントリ識別子も保持する必要がありますが、必須ではありません。
  
メッセージを移動またはコピーするときに通知を送信します。そのため、クライアントは、メッセージ ' [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドへの呼び出しが失敗する可能性があることを forewarned します。 
  
コピー操作または移動操作では、メッセージの状態は含まれません。 メッセージの状態を移動またはコピーすると、パフォーマンスに大きく影響します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**imapifolder:: copymessages**を使用して、メッセージが親フォルダーによってグループ化されることが多い検索結果フォルダーを作成します。 
  
これらの戻り値は、次の条件に当てはまることが予想されます。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**imapifolder:: copymessages**は、すべてのメッセージで正常にコピーまたは移動されました。  <br/> |S_OK  <br/> |
|**imapifolder:: copymessages**は、すべてのメッセージを正常にコピーまたは移動できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**imapifolder:: copymessages**を完了できませんでした。  <br/> |任意のエラー値  <br/> |
   
**imapifolder:: copymessages**を完了できない場合は、作業が行われていないと仮定しません。 **imapifolder:: copymessages**は、エラーが発生する前に1つ以上のメッセージをコピーまたは移動できる可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

