---
title: PidLidContactCharacterSet 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384865"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a>PidLidContactCharacterSet 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この連絡先に使用する文字セットを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidContactCharSet  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008023  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>備考

アプリケーションは、 **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md))、 **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) と**dispidFileUnderId のオプションの文字セットの依存リストを生成する場合に支援するためにこのプロパティを使用することができます。**([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) のプロパティです。 プロパティの値が"0x00000000"または"0x00000001"の場合は、アプリケーションとして設定されていないプロパティを扱う必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

