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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319706"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a>PidLidContactCharacterSet 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この連絡先に使用する文字セットを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidcontactcharset  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x00008023  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

アプリケーションは、このプロパティを使用して、 **dispidfileunder** [PidLidFileUnder](pidlidfileunder-canonical-property.md))、 **dispidfileunder 使用リスト**([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md))、dispidfileunder id の選択に関する、文字セット依存リストの生成を支援します。 ****([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) プロパティ。 プロパティの値が "0x00000000" または "0x00000001" の場合、アプリケーションはプロパティを未設定として扱う必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

