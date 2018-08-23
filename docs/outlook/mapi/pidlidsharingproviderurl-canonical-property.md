---
title: PidLidSharingProviderUrl 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingProviderUrl
api_type:
- COM
ms.assetid: d217ab33-d697-4d27-a962-08d551d301f0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1b906ce83e26326755b483382eec8e494cbe7875
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577367"
---
# <a name="pidlidsharingproviderurl-canonical-property"></a>PidLidSharingProviderUrl 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
共有プロバイダーに関連する、 **dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)) のプロパティで指定された URL を指定します。 これは、共有メッセージのプロパティです。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSharingProviderUrl  <br/> |
|プロパティを設定します。  <br/> |PSETID_Sharing  <br/> |
|長い ID (LID):  <br/> |0x00008A03  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、共有プロバイダーに関する詳細情報を提供するために使用が一般的にですが、無視する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でのメールボックスのフォルダーを共有します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

