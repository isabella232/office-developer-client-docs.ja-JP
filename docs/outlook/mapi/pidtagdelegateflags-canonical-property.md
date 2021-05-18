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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359900"
---
# <a name="pidtagdelegateflags-canonical-property"></a>PidTagDelegateFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
代理人が委任者のプライベート メッセージ オブジェクトを表示できるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|識別子:  <br/> |0x686B  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |メッセージ クラス定義の送信可能  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの各エントリは、次のいずれかの値に設定する必要があります。
  
|**Flag**|**値**|**説明**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |代理人は、プライベート メッセージ オブジェクトの表示を許可しない必要があります。  <br/> |
|ShowPrivate  <br/> |1  <br/> |代理人は、プライベート メッセージ オブジェクトの表示を許可する必要があります。  <br/> |
   
このプロパティは、デリゲート情報オブジェクトで設定する必要があります。 "ShowPrivate" の値は、ユーザーがプライベート メッセージ オブジェクトを表示する必要がある場合を示します。 この基本設定は、代理人がレビューアー、作成者、または編集者の役割を持つすべてのフォルダーに適用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

