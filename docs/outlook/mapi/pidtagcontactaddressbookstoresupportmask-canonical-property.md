---
title: PidTagContactAddressBookStoreSupportMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fb40e2c191056fe164c6a06bfdcf4b8e3d6eb92c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434439"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>PidTagContactAddressBookStoreSupportMask 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先フォルダーを **PR_STORE_SUPPORT_MASK** ストアから取得したプロパティ [(PidTagStoreSupportMask)](pidtagcontactaddressbookstoresupportmask-canonical-property.md)プロパティを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|識別子:  <br/> |0x6611  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |連絡先アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

連絡先アドレス帳プロバイダーは、このプロパティを使用して、ストアでサポートされている機能の不備を評価します。 これは、連絡先アドレス帳コンテナーのプロパティであり、連絡先アドレス帳コンテナーのテーブル内の列です。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

