---
title: MAPI 進行状況インジケーター
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410708"
---
# <a name="mapi-progress-indicators"></a>MAPI 進行状況インジケーター

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントに対して実行する操作の多くは、完了するまでに長い時間がかかることがあります。 時間のかかる操作の進行状況をクライアントに通知するために、操作の開始からその完了までの任意の時点で、操作の完了部分をグラフィカルに表示するインジケーターを表示することができます。 進行状況インジケーターは、完了する合計操作のパーセンテージを示しています。
  
次のメソッドは、時間のかかる操作と進行状況インジケーターの表示をサポートしています。
  
- [imapifolder:: copymessages](imapifolder-copymessages.md)、 [imapifolder:: copymessages](imapifolder-copyfolder.md)、imapifolder: [:D eletemessages](imapifolder-deletemessages.md)、imapifolder:: [eletefolder](imapifolder-deletefolder.md)、imapifolder [:: emptyfolder](imapifolder-emptyfolder.md)、 [imapifolder:: setreadflags](imapifolder-setreadflags.md)。
    
- [imapiprop:: copyprops](imapiprop-copyprops.md)および[imapiprop:: CopyTo](imapiprop-copyto.md)。
    
- [imapisupport::D ocopyprops](imapisupport-docopyprops.md)、 [imapisupport::D ocopyto](imapisupport-docopyto.md)、 [imapisupport:: copyfolder](imapisupport-copyfolder.md)、 [imapisupport:: copymessages](imapisupport-copymessages.md)。
    
- [IMessage::D eleteattach](imessage-deleteattach.md)。
    
- [IABContainer:: copyentries](iabcontainer-copyentries.md)。
    
進行状況インジケーターを表示するために、MAPI は progress オブジェクトを定義します。 Progress オブジェクトは、インジケーターの範囲を確立し、表示を作成するためのメソッドを含む[imapiprogress: IUnknown](imapiprogressiunknown.md)インターフェイスを実装します。 MAPI では、一部のクライアントと同様に、進行状況オブジェクトの実装が提供されます。 クライアントの実装 (指定されている場合) は、操作を実行するメソッドへの入力パラメーターとして使用する必要があります。 クライアントが progress オブジェクトへのポインターの代わりに NULL を渡す場合は、 [imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドを呼び出して MAPI の実装を使用します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

