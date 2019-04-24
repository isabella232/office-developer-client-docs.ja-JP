---
title: PidTagProfileServerFullVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341602"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>PidTagProfileServerFullVersion 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル内のアカウントが接続されている Microsoft Exchange Server の完全なバージョンとビルド情報を指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|識別子:  <br/> |0x663b  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>解説

プロファイルは、exchange サーバーに接続する1つ以上のアカウントを指定できますが、それらは同じ exchange サーバーに接続されている必要があります。
  
Microsoft Office outlook 2007 より前のバージョンの outlook では、このプロパティはサポートされていません。 これらのバージョンの Outlook では、プロファイルに**[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** が存在するかどうかを確認します。 
  
通常、アクティブなメールボックスが exchange サーバーに接続されている場合、Outlook 2007 は、アクティブなプロファイルの**PR_PROFILE_SERVER_FULL_VERSION**プロパティに、exchange server の完全なバージョン情報を格納します。 Outlook は、メジャーとマイナーのバージョン番号とメジャーおよびマイナーのビルド番号を含む**EXCHANGE_STORE_VERSION_NUM**構造体に情報を格納します。 たとえば、 **8.0.685.24**の Exchange Server バージョン識別子を格納するために、メジャーバージョン番号は8、マイナーバージョン番号は0、メジャービルド番号は685、マイナービルド番号は24です。
  
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

