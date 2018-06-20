---
title: プロファイルを削除します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799892"
---
# <a name="deleting-a-profile"></a>プロファイルを削除します。

  
  
**適用されます**: Outlook 
  
 **プロファイルを削除するには**
  
- [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md)を呼び出します。
    
 **DeleteProfile**は、現在使用されている、それを削除することが無効になるまで待機する場合、プロファイルの削除をマークします。 プロファイル実際には消えませんがアクティブなセッションを持つすべてのクライアントが切断されるまで。 
  
 **DeleteProfile** 、 _ulContext_パラメーターを MSG_SERVICE_DELETE を設定したプロファイルにすべてのメッセージ サービスのエントリ ポイント関数が呼び出されます。 エントリ ポイント関数への呼び出しは、サービスは、プロファイルから物理的に削除される前に発生します。 
  

