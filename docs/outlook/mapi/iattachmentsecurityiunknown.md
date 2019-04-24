---
title: iattachmentsecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326986"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft outlook 2010 および microsoft outlook 2013 ソリューションを使用して、添付ファイルが安全でないと見なされ、表示およびインデックス作成がブロックされているかどうかを確認します。
  
|||
|:-----|:-----|
|インターフェイス識別子:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |指定された添付ファイルが outlook 2010 または outlook 2013 によってブロックされているかどうかを確認し、表示およびインデックスを作成します。  <br/> |
   
## <a name="remarks"></a>解説

outlook 2010 および outlook 2013 ソリューションは、このインターフェイスを照会して、添付ファイルがブロックされているかどうかを確認できます。 outlook 2010 または outlook 2013 によってブロックされている添付ファイルは、outlook 2010 または outlook 2013 がどのように構成されているか、および管理者が適用したポリシーによって異なります。
  
## <a name="see-also"></a>関連項目



[MAPI 定数](mapi-constants.md)
  
[添付ファイルがブロックされていることを確認する](how-to-verify-an-attachment-is-blocked.md)

