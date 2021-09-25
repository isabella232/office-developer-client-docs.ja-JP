---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f20f891df60495407609653831e2442c9167dec2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592467"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ソリューションMicrosoft Outlook 2010およびMicrosoft Outlook 2013、添付ファイルが安全でないと見なされ、表示およびインデックス作成のためにブロックされるのを確認できます。
  
|||
|:-----|:-----|
|インターフェイス識別子:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |指定した添付ファイルが 2010 年または 2013 年Outlook 2013 年Outlook表示およびインデックス作成のためにブロックされている場合にチェックします。  <br/> |
   
## <a name="remarks"></a>注釈

Outlook 2010 および 2013 Outlook 2013 ソリューションでは、このインターフェイスに対してクエリを実行して、添付ファイルがブロックされるのを確認できます。 Outlook 2010 または Outlook 2013 によってブロックされる添付ファイルは、Outlook 2010 または Outlook 2013 の構成方法と管理者が適用したポリシーによって異なります。
  
## <a name="see-also"></a>関連項目



[MAPI 定数](mapi-constants.md)
  
[添付ファイルがブロックされているのを確認する](how-to-verify-an-attachment-is-blocked.md)

