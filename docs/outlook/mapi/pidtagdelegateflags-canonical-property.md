---
title: PidTagDelegateFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359900"
---
# <a name="pidtagdelegateflags-canonical-property"></a>PidTagDelegateFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
代理人が委任者のプライベートメッセージオブジェクトを表示できるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|識別子:  <br/> |0x686b  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |メッセージクラスで定義された、パススルーテーブル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの各エントリには、次のいずれかの値を設定する必要があります。
  
|**Flag**|**値**|**説明**|
|:-----|:-----|:-----|
|hideprivate  <br/> |.0  <br/> |代理人は、プライベートメッセージオブジェクトを表示できません。  <br/> |
|showprivate  <br/> |1-d  <br/> |代理人は、プライベートメッセージオブジェクトを表示することを許可されている必要があります。  <br/> |
   
このプロパティは、デリゲート情報オブジェクトで設定する必要があります。 "showprivate" という値は、委任者がプライベートメッセージオブジェクトを表示するように指定していることを示します。 この設定は、代理人が校閲者、作成者、または編集者の役割を持つすべてのフォルダーに適用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

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

