---
title: FlushQueues メソッドの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e5c78c71f7fddb04d3517aca0a34efa151ece08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411779"
---
# <a name="implementing-the-flushqueues-method"></a>FlushQueues メソッドの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーは [、IXPLogon::FlushQueues](ixplogon-flushqueues.md) メソッドを使用して、保留中のメッセージをトランスポート プロバイダー間でダウンロードしてアップロードします。 通常、MAPI スプーラーは、セッションにログオンしているすべてのトランスポート プロバイダーのキューをフラッシュします。最初のトランスポート プロバイダーは、ユーザーのプロファイルのトランスポート注文セクションで設定されています。 キューのフラッシュは、ほとんどの場合、ユーザーが直接要求した結果なので、キューのフラッシュ中のメッセージの送受信は MAPI スプーラーと同期します。 これらの呼び出しは同期的なので、トランスポート プロバイダーはそれらを可能な限り迅速に処理する必要があります。 
  
トランスポート プロバイダーは、適切なメッセージ処理を有効にし、MAPI スプーラーの **FlushQueues** 操作の一部として他のトランスポート プロバイダーが使用するモデムなどの外部リソースを有効にするには、次の手順に従って **FlushQueues** 呼び出しを処理する必要があります。 
  
|**手順**|**コンポーネント**|**実装**|
|:-----|:-----|:-----|
|1.  <br/> |MAPI スプーラー  <br/> |ユーザーのプロファイルのトランスポートの順序でリストされている最初のトランスポート プロバイダーの **FlushQueues** メソッドを呼び出し、要求されたフラグを  _ulFlags_ パラメーターに渡します。 **FlushQueues は、** アップロードおよびダウンロード操作全体に対してすべてのフラグが設定された 1 回呼び出されます。  <br/> |
|2。  <br/> |トランスポート プロバイダー  <br/> |FlushQueues 呼び出しから戻る前に、多くの **ことを行う必要** があります。 以前に送信されたメッセージが延期されている場合は [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを呼び出し、NOTIFY_SENT_DEFERREDする必要があります。 MAPI スプーラーは、トランスポート プロバイダーがメッセージの処理を終了する前に延期されたメッセージを取り消す可能性があります。  <br/> トランスポート プロバイダーがモデムなどの外部リソースを使用する場合は、外部リソースへの接続を確立する必要があります。  <br/> トランスポート プロバイダー STATUS_OUTBOUND_FLUSH行の **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティのビットは [、IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを使用して設定する必要があります。  <br/> その後、トランスポート プロバイダーは **FlushQueues S_OKを返す必要** があります。  <br/> |
|3。  <br/> |MAPI スプーラー  <br/> |トランスポート プロバイダーの状態行で STATUS_OUTBOUND_FLUSH ビットを確認し、キュー内の最初のメッセージに対して [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) を呼び出します。  <br/> |
|4.  <br/> |トランスポート プロバイダー  <br/> |メッセージを処理し **、SubmitMessage 呼び出しから返** します。  <br/> |
|5.  <br/> |MAPI スプーラー  <br/> |トランスポート プロバイダーが **SubmitMessage** から S_OKを返す場合、MAPI スプーラーは通常のメッセージ送信と同様に、メッセージの [IXPLogon::EndMessage](ixplogon-endmessage.md) を呼び出します。  <br/> トランスポート プロバイダーが **SubmitMessage** から S_OK 以外の値を返す場合、MAPI スプーラーは EndMessage を呼び出す前、または **SubmitMessage** を再度呼び出す前に値を適切に処理します。   <br/> |
|6.  <br/> |トランスポート プロバイダー  <br/> |_lpulFlags_ パラメーターのメッセージ処理状態を持つ **EndMessage** から返します。  <br/> |
|7.  <br/> |MAPI スプーラーとトランスポート プロバイダー  <br/> |**SubmitMessage** -  **EndMessage** ループは、キュー内のすべてのメッセージがダウンロードされるまで続行されます。  <br/> |
|8.  <br/> |MAPI スプーラー  <br/> |トランスポート プロバイダーの [IXPLogon::TransportNotify](ixplogon-transportnotify.md) メソッドを呼び出して、メッセージのダウンロードが完了したとトランスポート プロバイダー NOTIFY_END_OUTBOUND_FLUSHします。  <br/> |
|9.  <br/> |トランスポート プロバイダー  <br/> |送信メッセージの送信に使用される外部リソースを解放し、他のトランスポート プロバイダーがキューをフラッシュするために使用できます。  <br/> トランスポート プロバイダー STATUS_INBOUND_FLUSHの PR_STATUS_CODE **プロパティの** ビットは **、ModifyStatusRow を使用して設定する必要があります**。  <br/> |
|10.  <br/> |MAPI スプーラー  <br/> |トランスポート プロバイダーの状態の行で、STATUS_INBOUND_FLUSHビットを確認し、設定されている場合は [IXPLogon::StartMessage](ixplogon-startmessage.md) を呼び出します。  <br/> |
|11.  <br/> |トランスポート プロバイダー  <br/> |メッセージを処理し **、StartMessage から返します**。 トランスポート プロバイダーにアップロードする他のメッセージがある場合は、スプーラー **Notify** を呼び出し、NOTIFY_NEWMAILする必要があります。  <br/> トランスポート プロバイダーにアップロードするメッセージがない場合は **、STARTMessage** で渡された MAPI スプーラーがメッセージに対して [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出して返す必要があります。  <br/> |
|12.  <br/> |MAPI スプーラー  <br/> |メッセージで **SaveChanges** が呼び **出されるまで、StartMessage** の呼び出しを続行します。 トランスポート プロバイダーのアップロードが完了すると、MAPI スプーラーは **TransportNotify** を呼び出し、NOTIFY_END_INBOUND_FLUSH設定します。  <br/> |
|13.  <br/> |トランスポート プロバイダー  <br/> |**ModifyStatusRow** を使用して、状態行の **PR_STATUS_CODE** プロパティの STATUS_INBOUND_FLUSH ビットをクリアし、すべての外部リソースを解放して、他のトランスポート プロバイダーが使用できます。  <br/> |
|14.  <br/> |MAPI スプーラー  <br/> |ユーザー **のプロファイルのトランスポート** 順序で一覧表示されている次のトランスポート プロバイダーの FlushQueues を呼び出します。  <br/> |
   
クライアント アプリケーションがトランスポート プロバイダーの状態オブジェクトで [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) を呼び出す場合、トランスポート プロバイダーは **ModifyStatusRow** を使用して状態行に適切なビットを設定する必要があります。 MAPI スプーラーは、MAPI スプーラーの便宜上、トランスポート プロバイダーの **IXPLogon::FlushQueues** メソッドを呼び出します。 クライアント アプリケーションの **IMAPIStatus::FlushQueues** 呼び出しの結果としてトランスポート プロバイダーの **IXPLogon::FlushQueues** メソッドが呼び出された場合、この操作はクライアント アプリケーションに対して非同期的に行われます。 それ以外 **の場合、IXPLogon::FlushQueues は** MAPI スプーラーと同期して動作します。 
  
パフォーマンス上の理由から、MAPI スプーラーは、トランスポート プロバイダーの状態行に STATUS_INBOUND_FLUSH フラグと STATUS_OUTBOUND_FLUSH フラグが設定されている場合にのみ、トランスポート プロバイダーの **FlushQueues** メソッドを呼び出します。 したがって、トランスポート プロバイダーは、状態行の STATUS_OUTBOUND_FLUSH フラグとSTATUS_INBOUND_FLUSHをクリアすることで **、FlushQueues** 操作をいつでも停止できます。 MAPI スプーラーがシャットダウン中で **、FlushQueues** 操作を終了する必要がある場合は、トランスポート **Notify** を呼び出し、NOTIFY_END_INBOUND_FLUSH フラグと NOTIFY_END_OUTBOUND_FLUSH フラグの両方を設定します。 トランスポート プロバイダーは、すべての外部リソースを解放して返す必要があります。 
  

