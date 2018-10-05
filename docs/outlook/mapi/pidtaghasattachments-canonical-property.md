---
title: PidTagHasAttachments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aca9c9f9c22fc4057f1650d1342492d2ed34653c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397605"
---
# <a name="pidtaghasattachments-canonical-property"></a>PidTagHasAttachments 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージには、少なくとも 1 つの添付ファイルが含まれている場合、TRUE が格納されます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_HASATTACH  <br/> |
|識別子:  <br/> |0x0E1B  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

メッセージ ・ ストアでは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティの**MSGFLAG_HASATTACH**フラグのこのプロパティをコピーします。 クライアント アプリケーションは、メッセージ ビューアーで、メッセージの添付ファイルを並べ替えるには、 **PR_HASATTACH**を使用できます。 
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを使用してこのプロパティを更新する値です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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

