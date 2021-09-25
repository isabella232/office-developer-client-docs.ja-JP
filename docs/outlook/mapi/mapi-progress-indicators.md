---
title: MAPI 進行状況インジケーター
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d1317290b99fe3e10dec539e0a349382cc880188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575646"
---
# <a name="mapi-progress-indicators"></a>MAPI 進行状況インジケーター

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントに対して実行する操作の多くは、完了に長い時間がかかる場合があります。 長い操作の進行状況をクライアントに通知するには、操作の開始から完了まで、任意の時点で操作の終了部分をグラフィカルに表示するインジケーターを表示できます。 進行状況インジケーターには、完了する操作全体の割合が表示されます。
  
次のメソッドは、長い操作と進行状況インジケーターの表示をサポートします。
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps と](imapiprop-copyprops.md) [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport:::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
進行状況インジケーターを表示するために、MAPI は進行状況オブジェクトを定義します。 Progress オブジェクトは [、IMAPIProgress : IUnknown](imapiprogressiunknown.md) インターフェイス、インジケーターの範囲を確立し、ディスプレイを作成するためのメソッドを含むインターフェイスを実装します。 MAPI は、一部のクライアントと同様に進行状況オブジェクトの実装を提供します。 クライアントの実装が指定されている場合は、操作を実行するメソッドの入力パラメーターとして使用する必要があります。 クライアントが進行状況オブジェクトへのポインターではなく NULL を渡す場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) メソッドを呼び出して MAPI の実装を使用します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

