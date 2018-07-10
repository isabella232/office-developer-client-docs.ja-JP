---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a8e353bbb4f276169ae26ba9d05821158bf55f00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801194"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**適用されます**: Outlook 
  
サーバーに送信するメッセージをスプールする Outlook プロトコル マネージャーをエミュレートするためにローカル ストアを設定します。
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in]ローカル ストアはスプーラーをエミュレートする必要がある場合、このパラメーターを True に設定します。そうでない場合は、False に設定します。 
    
## <a name="remarks"></a>備考

ローカル ストアは、Outlook プロトコル マネージャーとして、処理のためのバックエンドのサーバー (たとえば、MSN のサーバーまたは AOL サーバー) に送信キューにメッセージをスプールを動作するように**IPSTX::EmulateSpooler**を呼び出します。 スプーラーをエミュレートする、同期中に、ストアはし、これら 2 つのメソッドを呼び出します。 
  
1. ストア内のメッセージの送信キューを取得するのには**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** にします。 このメソッドは、ストアは、Outlook プロトコル マネージャーをエミュレートする場合にのみ成功します。 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** をサーバーに送信する前に、発信キュー内のメッセージにのみアクセスをセキュリティで保護します。 このメソッドは、ストアは、Outlook プロトコル マネージャーをエミュレートする場合にのみ成功します。 メッセージを送信すると、ストアへの唯一のアクセス権を解放するには、再度このメソッドを呼び出します。 
    
> [!NOTE]
> Outlook 2002 年以降、Outlook プロトコル マネージャーは MAPI スプーラーを交換してくださいし、バック エンド サーバーに送信メッセージのスプールの担当するようになりました。 
  
## <a name="see-also"></a>関連項目



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)
