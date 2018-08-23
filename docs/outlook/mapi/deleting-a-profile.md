---
title: プロファイルの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573244"
---
# <a name="deleting-a-profile"></a>プロファイルの削除

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **プロファイルを削除するには**
  
- [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md)を呼び出します。
    
 **DeleteProfile**は、現在使用されている、それを削除することが無効になるまで待機する場合、プロファイルの削除をマークします。 プロファイル実際には消えませんがアクティブなセッションを持つすべてのクライアントが切断されるまで。 
  
 **DeleteProfile** 、 _ulContext_パラメーターを MSG_SERVICE_DELETE を設定したプロファイルにすべてのメッセージ サービスのエントリ ポイント関数が呼び出されます。 エントリ ポイント関数への呼び出しは、サービスは、プロファイルから物理的に削除される前に発生します。 
  

