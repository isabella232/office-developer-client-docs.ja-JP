---
title: PidTagMessageSize 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355651"
---
# <a name="pidtagmessagesize-canonical-property"></a>PidTagMessageSize 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージオブジェクトのすべてのプロパティのサイズの合計 (バイト数) を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_SIZE  <br/> |
|識別子:  <br/> |0x0e08  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージオブジェクトに公開することをお勧めします。 メッセージサイズは、メッセージがあるメッセージストアから別のメッセージストアに移動されたときに転送されるおおよそのバイト数を示します。 message オブジェクトのすべてのプロパティのサイズの合計は、通常、メッセージテキストだけではなく、非常に大きくなります。 
  
ほとんどのメッセージストアプロバイダーは、処理するメッセージに対してこのプロパティを計算します。 ただし、一部のメッセージストアプロバイダーでは、このプロパティをサポートしていません。 いずれの場合も、このプロパティは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)または[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出されるまで使用できません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コアメッセージストアオブジェクトに対する許容される操作を指定します。
    
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

