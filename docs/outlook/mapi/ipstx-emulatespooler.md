---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a630db9edb03c67f1f8e2c7a3b19088a88b1123b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620507"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メッセージをサーバーにスプールOutlookプロトコル マネージャーをエミュレートするローカル ストアを設定します。
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in]ローカル ストアでスプーラーをエミュレートする場合は、このパラメーターを True に設定します。設定しない場合は False に設定します。 
    
## <a name="remarks"></a>注釈

ローカル ストアは **IPSTX::EmulateSpooler** を呼び出して Outlook プロトコル マネージャーとして機能し、送信キュー内のメッセージを処理のためにバック エンド サーバー (MSN サーバーや AOL サーバーなど) にスプールします。 同期中にスプーラーを表示すると、ストアは次の 2 つのメソッドを呼び出します。 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** を使用して、ストア内のメッセージの送信キューを取得します。 このメソッドは、ストアがプロトコル マネージャーのOutlook成功します。 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** を使用して、送信キュー内のメッセージへの唯一のアクセスをサーバーに送信する直前にセキュリティで保護します。 このメソッドは、ストアがプロトコル マネージャーのOutlook成功します。 メッセージを送信した後、ストアはもう一度このメソッドを呼び出して、そのメソッドへの唯一のアクセス権を解放します。 
    
> [!NOTE]
> 2002 Outlook以降、Outlook プロトコル マネージャーは MAPI スプーラーを置き換え、送信メッセージをバック エンド サーバーにスプールする責任を負いました。 
  
## <a name="see-also"></a>関連項目



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

