---
title: PidTagAttachTransportName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361069"
---
# <a name="pidtagattachtransportname-canonical-property"></a>PidTagAttachTransportName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
TNEF メッセージに関連付けることができるように変更された添付ファイルの名前が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_TRANSPORT_NAME、PR_ATTACH_TRANSPORT_NAME_A、PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|識別子:  <br/> |0x370c  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

TNEF とトランスポートプロバイダーは、これらのプロパティを使用します。 通常、クライアントアプリケーションでは使用できません。 
  
これらのプロパティは、基になるメッセージングシステムが提供されたファイル名をサポートしていない場合に、TNEF でよく使用されます。 たとえば、ユーザーが同じ名前で複数のファイルを添付する場合に使用されます (CONFIG という名前のファイルが5つある場合など)。disk.sys. トランスポートプロバイダーが一意であることを確認するには、名前を変更する必要があります。 変更された各名前は、その添付ファイルの**PR_ATTACH_TRANSPORT_NAME**および関連するプロパティに表示されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

