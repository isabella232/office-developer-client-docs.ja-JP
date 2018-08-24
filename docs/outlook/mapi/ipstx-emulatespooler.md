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
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580720"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サーバーに送信するメッセージをスプールする Outlook プロトコル マネージャーをエミュレートするためにローカル ストアを設定します。
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in]ローカル ストアはスプーラーをエミュレートする必要がある場合、このパラメーターを True に設定します。そうでない場合は、False に設定します。 
    
## <a name="remarks"></a>注釈

ローカル ストアは、Outlook プロトコル マネージャーとして、処理のためのバックエンドのサーバー (たとえば、MSN のサーバーまたは AOL サーバー) に送信キューにメッセージをスプールを動作するように**IPSTX::EmulateSpooler**を呼び出します。 スプーラーをエミュレートする、同期中に、ストアはし、これら 2 つのメソッドを呼び出します。 
  
1. ストア内のメッセージの送信キューを取得するのには**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** にします。 このメソッドは、ストアは、Outlook プロトコル マネージャーをエミュレートする場合にのみ成功します。 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** をサーバーに送信する前に、発信キュー内のメッセージにのみアクセスをセキュリティで保護します。 このメソッドは、ストアは、Outlook プロトコル マネージャーをエミュレートする場合にのみ成功します。 メッセージを送信すると、ストアへの唯一のアクセス権を解放するには、再度このメソッドを呼び出します。 
    
> [!NOTE]
> Outlook 2002 年以降、Outlook プロトコル マネージャーは MAPI スプーラーを交換してくださいし、バック エンド サーバーに送信メッセージのスプールの担当するようになりました。 
  
## <a name="see-also"></a>関連項目



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

