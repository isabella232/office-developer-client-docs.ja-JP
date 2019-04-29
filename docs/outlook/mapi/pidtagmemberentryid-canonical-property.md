---
title: PidTagMemberEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433039"
---
# <a name="pidtagmemberentryid-canonical-property"></a>PidTagMemberEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
システムアクセス制御リスト (SACL) テーブルメンバーのディレクトリオブジェクトエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFF  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、 [IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスで、SACL が適用される個人または役割を一意に識別するために使用されます。 SACL テーブルにメンバーを作成した後は、 **ENTRYID**を変更することはできません。 変更するには、table メンバーを削除して、別の**ENTRYID**で再作成する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

