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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392278"
---
# <a name="pidtagdelegateflags-canonical-property"></a>PidTagDelegateFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
代理人が代理人の秘密のメッセージ オブジェクトを表示するかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|識別子:  <br/> |0x686B  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |クラスによって定義されたメッセージ送信できます。  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの各エントリを次の値のいずれかに設定する必要があります。
  
|**Flag**|**値**|**説明**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |プライベート メッセージ オブジェクトを表示するのにはデリゲートを使用できませんする必要があります。  <br/> |
|ShowPrivate  <br/> |1  <br/> |デリゲートは、オブジェクトのプライベート メッセージを表示するのにはできます。  <br/> |
   
代理人の情報オブジェクトにこのプロパティを設定する必要があります。 "ShowPrivate"の値は、オブジェクトのプライベート メッセージが表示されるようにするのには、代理人が要求していることを示します。 この設定は、代理人の校閲者、作成者、または編集者の役割を持っているすべてのフォルダーに適用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。
    
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

