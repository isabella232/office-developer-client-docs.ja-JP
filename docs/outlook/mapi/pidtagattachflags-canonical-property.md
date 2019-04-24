---
title: PidTagAttachFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339334"
---
# <a name="pidtagattachflags-canonical-property"></a>PidTagAttachFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのフラグのビットマスクを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_FLAGS  <br/> |
|識別子:  <br/> |0x3714  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、MHTML サポートに使用されます。 
  
**PR_ATTACH_FLAGS**ビットマスクには、次の1つ以上のフラグを設定できます。 
  
ATT_INVISIBLE_IN_HTML 
  
> この添付ファイルは、HTML レンダリングアプリケーションでは使用できず、多目的インターネットメール Extensions (MIME) 処理で無視する必要があることを示します。 
    
ATT_INVISIBLE_IN_RTF 
  
> この添付ファイルは、リッチテキスト形式 (RTF) のアプリケーションでは使用できず、MAPI で無視する必要があることを示します。
    
**PR_ATTACH_FLAGS**プロパティが0に設定されているか、存在しない場合、添付ファイルはすべてのアプリケーションによって処理されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
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

