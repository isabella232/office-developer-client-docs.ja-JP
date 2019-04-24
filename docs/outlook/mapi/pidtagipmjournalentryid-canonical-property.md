---
title: PidTagIpmJournalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmJournalEntryId
api_type:
- HeaderDef
ms.assetid: a3765b9d-a108-46d7-a97c-a825ae3980be
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b5dfc378a2558e906bec018608e2d2c776090c06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327910"
---
# <a name="pidtagipmjournalentryid-canonical-property"></a>PidTagIpmJournalEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Outlook Journal フォルダーの**EntryID**が保存されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_JOURNAL_ENTRYID  <br/> |
|識別子:  <br/> |0x36D2  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |フォルダー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、受信トレイフォルダー、およびメッセージストアのルートフォルダーに格納されます。 特定のメッセージストアのプロパティにアクセスするには、次の手順を実行します。 
  
1. 最初に、[受信トレイ] フォルダー内のプロパティを探します。 [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を使用して、受信トレイフォルダーの**EntryID**への参照を取得します。 
    
2. **IMsgStore:: getreceivefolder**が成功した場合は、inbox および[IMsgStore:: openentry](imsgstore-openentry.md)の**EntryID**への参照を使用して、受信トレイを開き、 **imapifolder**オブジェクトへの参照を取得します。 
    
3. **IMsgStore:: openentry**に成功した場合は、返された参照を**imapifolder**オブジェクトと[imapifolder:: GetProps](imapiprop-getprops.md)を使用して、目的のプロパティを取得します。 
    
4. 手順1、2、または3が失敗した場合は、ルートフォルダー内のプロパティを探します。 これを行うには、 **IMsgStore:: openentry**を使用して**l tryid**に NULL を指定し、メッセージストアのルートフォルダーを開き、 **imapifolder**オブジェクトへの参照を取得します。 
    
5. ルートフォルダーを正常に開くことができた場合は、返された参照を**imapifolder**オブジェクトと**imapifolder:: GetProps**を使用して取得し、目的のプロパティを取得します。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。
    
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

