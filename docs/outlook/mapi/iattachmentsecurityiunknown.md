---
title: IAttachmentSecurity IUnknown
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
ms.openlocfilehash: f182610f9cf4874cc18c409960e1f8b23f853d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574827"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルが安全でないと表示して、インデックス作成のブロックと見なされますかどうかを確認する Microsoft Outlook 2010、Outlook 2013 のマイクロソフトのソリューションを使用できます。
  
|||
|:-----|:-----|
|インターフェイスの識別子。  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |指定した添付ファイルが表示して、インデックス作成の Outlook 2010 または Outlook 2013 でブロックされているかどうかを確認します。  <br/> |
   
## <a name="remarks"></a>注釈

Outlook 2010、Outlook 2013 のソリューションでは、添付ファイルがブロックされているかどうかを確認するには、このインターフェイスを照会できます。 Outlook 2010 または Outlook 2013 でブロックされる添付ファイルは、どのように Outlook 2010 または Outlook 2013 が構成され、管理者が適用するポリシーによって異なります。
  
## <a name="see-also"></a>関連項目



[MAPI �萔](mapi-constants.md)
  
[添付がプロセスされていることを確認する](how-to-verify-an-attachment-is-blocked.md)

