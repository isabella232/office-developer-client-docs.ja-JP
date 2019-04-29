---
title: PidTagContactAddressBookStoreSupportMasks 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMasks
api_type:
- HeaderDef
ms.assetid: 68f5aac1-714c-48fc-a0cf-a0c0401a6070
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e06d9a3ee2352e05e38ab1f2d86014f970160f9d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427802"
---
# <a name="pidtagcontactaddressbookstoresupportmasks-canonical-property"></a>PidTagContactAddressBookStoreSupportMasks 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストアのサポートされている機能を示すフラグを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_STORE_SUPPORT_MASKS  <br/> |
|識別子:  <br/> |0x6621  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、連絡先フォルダーを含むストアから取得されます。 連絡先アドレス帳プロバイダーは、これを使用して、ストアのサポートされている機能の adequacy を評価します。 これは、連絡先のアドレス帳の [プロファイル] セクションのプロパティです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

