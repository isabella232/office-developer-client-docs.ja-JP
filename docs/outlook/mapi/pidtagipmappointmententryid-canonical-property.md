---
title: PidTagIpmAppointmentEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmAppointmentEntryId
api_type:
- HeaderDef
ms.assetid: a6e8c8fb-b76a-4a73-b112-6399e4d94233
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d27506edf6eb40f6b244733336b8b381ea941442
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384760"
---
# <a name="pidtagipmappointmententryid-canonical-property"></a>PidTagIpmAppointmentEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Outlook の予定表フォルダーの**エントリ Id**が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_APPOINTMENT_ENTRYID  <br/> |
|識別子:  <br/> |0x36D0  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、[受信トレイ] フォルダーで、メッセージ ・ ストアのルート フォルダーに格納されます。 特定のメッセージ ストアのプロパティにアクセスするには、次の。 
  
1. 最初に、受信トレイ フォルダー内のプロパティを探します。 [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を使用すると、受信トレイ フォルダーの**エントリ Id**への参照を取得します。 
    
2. **IMsgStore::GetReceiveFolder**が成功した場合は、受信トレイを開き、 **IMAPIFolder**オブジェクトへの参照を取得する、受信トレイと[IMsgStore::OpenEntry](imsgstore-openentry.md)の**エントリ Id**への参照を使用します。 
    
3. **IMsgStore::OpenEntry**が成功した場合は、目的のプロパティを取得する**IMAPIFolder**オブジェクトと[IMAPIProp::GetProps](imapiprop-getprops.md)に返される参照を使用します。 
    
4. 1、2、または 3 の手順が失敗した場合は、ルート フォルダーのプロパティを検索します。 そのためには、 **IMsgStore::OpenEntry**、 **lpEntryID**のメッセージ ・ ストアのルート フォルダーを開き、 **IMAPIFolder**オブジェクトへの参照を取得するのには NULL を指定するを使用します。 
    
5. ルート フォルダーを開くときに成功した場合は、目的のプロパティを取得するのには、 **IMAPIFolder**オブジェクトと**IMAPIProp::GetProps**に返される参照を使用します。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

