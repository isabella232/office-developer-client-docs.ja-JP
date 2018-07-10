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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800391"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity: IUnknown

  
  
**適用されます**: Outlook 
  
添付ファイルが安全でないと表示して、インデックス作成のブロックと見なされますかどうかを確認する Microsoft Outlook 2010、Outlook 2013 のマイクロソフトのソリューションを使用できます。
  
|||
|:-----|:-----|
|インターフェイスの識別子。  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |指定した添付ファイルが表示して、インデックス作成の Outlook 2010 または Outlook 2013 でブロックされているかどうかを確認します。  <br/> |
   
## <a name="remarks"></a>備考

Outlook 2010、Outlook 2013 のソリューションでは、添付ファイルがブロックされているかどうかを確認するには、このインターフェイスを照会できます。 Outlook 2010 または Outlook 2013 でブロックされる添付ファイルは、どのように Outlook 2010 または Outlook 2013 が構成され、管理者が適用するポリシーによって異なります。
  
## <a name="see-also"></a>関連項目



[MAPI �萔](mapi-constants.md)
  
[添付ファイルがブロックされていることを確認します。](how-to-verify-an-attachment-is-blocked.md)
