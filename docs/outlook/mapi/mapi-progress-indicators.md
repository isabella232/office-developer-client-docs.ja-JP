---
title: MAPI の進捗状況
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d8af2ba3067dabe759056313eb278b9901510980
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801420"
---
# <a name="mapi-progress-indicators"></a>MAPI の進捗状況

  
  
**適用対象**: Outlook 
  
完了するのには時間がかかる多くのクライアントに対して実行する操作のことができます。 時間のかかる操作の進行状況をクライアントに通知をするには、任意の時点で、操作の開始からその終了時に視覚的に操作の完了部分を表示するインジケーターを表示できます。 進行状況のインジケーターは、合計の操作を完了するの割合を示しています。
  
次の方法では、時間のかかる操作と、進行状況インジケーターの表示をサポートします。
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)、 [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)、 [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)、 [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)、 [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)、および[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)。
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)と[IMAPIProp::CopyTo](imapiprop-copyto.md)。
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)、 [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)、 [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)、および[IMAPISupport::CopyMessages](imapisupport-copymessages.md)。
    
- [IMessage::DeleteAttach](imessage-deleteattach.md)。
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md)。
    
進行状況のインジケーターを表示するには、MAPI は、実行中のオブジェクトを定義します。 進行中のオブジェクトの実装、 [IMAPIProgress: IUnknown](imapiprogressiunknown.md)インタ フェース、インジケーターの範囲を確立して、表示を作成するためのメソッドを含むインターフェイスです。 MAPI は、一部のクライアントと同じように進行中のオブジェクトの実装を提供します。 いずれかが指定した場合、操作を実行するメソッドに入力パラメーターとして、クライアントの実装を使用してください。 クライアント実行中のオブジェクトへのポインターではなく NULL が成功した場合は、 [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出すことによって MAPI の実装を使用します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

