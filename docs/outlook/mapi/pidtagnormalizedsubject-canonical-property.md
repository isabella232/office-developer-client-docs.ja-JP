---
title: PidTagNormalizedSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329275"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>PidTagNormalizedSubject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プレフィックスが削除されたメッセージの件名を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NORMALIZED_SUBJECT、PR_NORMALIZED_SUBJECT_A、PR_NORMALIZED_SUBJECT_W  <br/> |
|識別子:  <br/> |0x0e1d  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |電子メール  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、次の方法で、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) および**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) プロパティから、メッセージストアまたはトランスポートプロバイダーによって計算されます。
  
- **PR_SUBJECT_PREFIX**が存在し、 **PR_SUBJECT**の初期部分文字列である場合、 **PR_NORMALIZED_SUBJECT**および関連付けられたプロパティは、プレフィックスが削除された**PR_SUBJECT**の内容に設定されます。 
    
- **PR_SUBJECT_PREFIX**が存在していても、 **PR_SUBJECT**の初期部分文字列ではない場合、 **PR_SUBJECT_PREFIX**は次のルールを使用して PR_SUBJECT から削除され、 **** から再計算されます。文字列が**PR_SUBJECT**に含まれている場合1 ~ 3 桁の数字以外の文字の後にコロンとスペースが続く場合、その文字列はコロンで始まり、空白はプレフィックスになります。 数字、空白文字、および句読点は、有効なプレフィックス文字ではありません。 
    
- **PR_SUBJECT_PREFIX**が存在しない場合は、前の手順で説明したルールを使用して、 **PR_SUBJECT**から計算されます。 このプロパティには、プレフィックスが削除された**PR_SUBJECT**の内容が設定されます。 
    
 **メモ****PR_SUBJECT_PREFIX**が空の文字列の場合、 **PR_SUBJECT**とこのプロパティは同じです。 
  
最終的に、このプロパティは**PR_SUBJECT**のプレフィックスに続く部分である必要があります。 プレフィックスがない場合、このプロパティは**PR_SUBJECT**と同じになります。
  
 **PR_SUBJECT_PREFIX**およびこのプロパティは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)実装の一部として計算する必要があります。 クライアントアプリケーションは、 **imapiprop:: SaveChanges**呼び出しによってコミットされるまで、値に対して[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを要求しません。 
  
件名のプロパティは通常、256文字未満の小さな文字列で、メッセージストアプロバイダーは、オブジェクトのリンクと埋め込み (OLE) **IStream**インターフェイスをサポートする義務を持ちません。 クライアントは、常に**imapiprop**インターフェイスを使用してアクセスを試行し、MAPI_E_NOT_ENOUGH_MEMORY が返された場合にのみ**IStream**に頼る必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
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

