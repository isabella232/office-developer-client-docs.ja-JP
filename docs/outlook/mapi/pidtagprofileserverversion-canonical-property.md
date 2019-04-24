---
title: PidTagProfileServerVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286567"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>PidTagProfileServerVersion 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft Outlook プロファイルのアカウントが接続されている microsoft Exchange Server のバージョンに関する情報を指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|識別子:  <br/> |0x661b  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>解説

プロファイルは、exchange サーバーに接続する1つ以上のアカウントを指定できますが、それらは同じ exchange サーバーに接続されている必要があります。
  
Microsoft Office outlook 2007 より前のバージョンの outlook では、このプロパティを書き込み、アクティブなプロファイルが接続されている Exchange サーバーのバージョンに関する情報を格納できます。 ただし、バージョン情報の形式は、Exchange Server のバージョンによって異なります。 たとえば、Outlook は**PR_PROFILE_SERVER_VERSION**に格納されている10進値6944で、Microsoft Exchange SERVER 2003 の**6.5.6944.3**のバージョン識別子のメジャービルド番号のみを表します。 Exchange 2007 接続の場合、Outlook は、メジャーバージョン番号とメジャービルド番号を、プロパティにこれらの数値を連結した16進形式で格納します。 **8.0.685.24**の Exchange 2007 バージョン id には、メジャーバージョン番号8とメジャービルド番号685が10進数で含まれています。 両方の数値を16進数に変換すると、0x8 と0x2ad が得られます。 これらの2つの数値を連結すると、Outlook では**PR_PROFILE_SERVER_VERSION**の値0x82ad が16進表現で格納されます。 
  
Outlook 2007 では、このプロパティの読み取りまたは書き込みは行われません。 **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** がサポートされています。 
  
**PR_PROFILE_SERVER_VERSION**または**PR_PROFILE_SERVER_FULL_VERSION**のいずれか1つだけがプロファイルに存在する可能性がありますが、プロファイルに常に存在する保証はありません。 Outlook は、Exchange サーバーに正常に接続されるまでは、どちらのプロパティにも書き込みを行いません。 
  
Outlook オブジェクトモデルでは、 **NameSpace**オブジェクトの**ExchangeMailboxServerVersion**プロパティを使用して、アクティブなメールボックスがホストされている Exchange サーバーのバージョンを検索できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義を提供します。
    
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

