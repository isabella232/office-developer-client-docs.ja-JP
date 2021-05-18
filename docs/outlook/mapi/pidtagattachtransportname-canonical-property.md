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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361069"
---
# <a name="pidtagattachtransportname-canonical-property"></a>PidTagAttachTransportName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
TNEF メッセージに関連付けできるよう変更された添付ファイルの名前が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_TRANSPORT_NAME、PR_ATTACH_TRANSPORT_NAME_A、PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|識別子:  <br/> |0x370C  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

TNEF とトランスポート プロバイダーは、これらのプロパティを使用します。 通常、クライアント アプリケーションでは使用できません。 
  
これらのプロパティは、基になるメッセージング システムが指定されたファイル名をサポートしていない場合に TNEF でよく使用されます。 たとえば、ユーザーが同じ名前の複数のファイルを添付する場合に使用されます (たとえば、5 つのファイルが CONFIG.SYS)。 トランスポート プロバイダーは、一意の名前を変更する必要があります。 変更された各名前は、添付ファイルのプロパティ **PR_ATTACH_TRANSPORT_NAMEプロパティ** に表示されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

