---
title: PidTagAdditionalRenEntryIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282362"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>PidTagAdditionalRenEntryIds 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の特別なフォルダーのエントリ id を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|識別子:  <br/> |0x36D8  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>解説

この複数値を持つプロパティの最初の5つのエントリは、ストア内に存在する場合は、次の特別なフォルダーに適用されます。
  
0-競合フォルダー
  
1-同期の問題フォルダー
  
2-ローカルエラーフォルダー
  
3-サーバーエラーフォルダー
  
4-迷惑メールフォルダー
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> 受信者を漏洩機密情報 (パスワードやその他の個人情報など) に信頼できないソースに誘導するように設計された電子メールメッセージを識別してマークします。
    
[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。
    
### <a name="header-files"></a>ヘッダーファイル

Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)


[ストア API について](https://msdn.microsoft.com/library/aa192884.aspx)

