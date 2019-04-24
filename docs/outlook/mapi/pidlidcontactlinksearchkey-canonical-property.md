---
title: PidLidContactLinkSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319776"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>PidLidContactLinkSearchKey 標準プロパティ

**適用対象**: Outlook 2013 | Outlook 2016 
  
この message オブジェクトでリンクされている連絡先の**searchkeys**のリストを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidcontactlinksearchkey  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008584  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

|**長さ (バイト数)**|**説明**|**メモ**|
|:-----|:-----|:-----|
|pbm-2  <br/> |contactentrycount  <br/> |なし  <br/> |
|変数  <br/> |searchkey データ  <br/> |contactentrycount 回数を繰り返します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目

- [MAPI のプロパティ](mapi-properties.md) 
- [MAPI 標準プロパティ](mapi-canonical-properties.md)
- [標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
- [MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

