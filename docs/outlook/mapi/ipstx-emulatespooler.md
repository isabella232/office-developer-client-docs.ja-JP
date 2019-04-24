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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315093"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Outlook プロトコルマネージャーをエミュレートして、送信メッセージをサーバーにスプールするように、ローカルストアを設定します。
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _femulate_
  
>  順番ローカルストアがスプーラーをエミュレートする必要がある場合は、このパラメーターを True に設定します。そうでない場合は False に設定します。 
    
## <a name="remarks"></a>解説

ローカルストアは**ipstx:: EmulateSpooler**を呼び出して、Outlook プロトコルマネージャーとして機能し、送信キュー内のメッセージをバックエンドサーバー (たとえば、MSN server または AOL サーバー) にスプールして処理します。 同期時にスプーラーをエミュレートすると、ストアは次の2つのメソッドを呼び出します。 
  
1. **[IMsgStore:: getoutgoingqueue](imsgstore-getoutgoingqueue.md)** ストア内のメッセージの送信キューを取得します。 このメソッドは、ストアが Outlook プロトコルマネージャーをエミュレートしている場合にのみ成功します。 
    
2. **[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** は、メッセージをサーバーに送信する直前に、送信キュー内のメッセージへのアクセスを保護します。 このメソッドは、ストアが Outlook プロトコルマネージャーをエミュレートしている場合にのみ成功します。 メッセージを送信した後、ストアはこのメソッドをもう一度呼び出して、単独でアクセス権を解放します。 
    
> [!NOTE]
> outlook 2002 以降、outlook プロトコルマネージャーは MAPI スプーラーを置き換え、送信メッセージをバックエンドサーバーにスプールする責任がありました。 
  
## <a name="see-also"></a>関連項目



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

