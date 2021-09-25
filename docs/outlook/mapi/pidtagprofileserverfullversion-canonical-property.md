---
title: PidTagProfileServerFullVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 66c6b8d50947baafb726c41c28e3bb4d675eab4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616419"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>PidTagProfileServerFullVersion 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル内のアカウントが接続されているMicrosoft Exchange Server完全なバージョンとビルド情報を指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|識別子:  <br/> |0x663B  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>注釈

プロファイルは、1 つのアカウントに接続する 1 つ以上のアカウントをExchange Server、同じアカウントに接続する必要Exchange Server。
  
2007 Outlook以前Microsoft Office Outlookバージョンでは、このプロパティはサポートされていません。 これらのバージョンのプロファイルOutlookプロファイル **[内にPR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** を確認します。 
  
通常、アクティブなメールボックスが Exchange Server に接続されている場合、Outlook 2007 は、Exchange Server バージョン情報をアクティブ プロファイルの **PR_PROFILE_SERVER_FULL_VERSION** プロパティに保存します。 Outlookは、メジャー バージョン番号とマイナー **バージョン番号EXCHANGE_STORE_VERSION_NUM** メジャービルド番号とマイナー ビルド番号を含むデータ構造に情報を格納します。 たとえば、Exchange Server バージョン識別子 **8.0.685.24** を格納するには、メジャー バージョン番号は 8、マイナー バージョン番号は 0、メジャー ビルド番号は 685、マイナー ビルド番号は 24 です。
  
プロファイル **にPR_PROFILE_SERVER_VERSIONまたは** PR_PROFILE_SERVER_FULL_VERSIONの1 つだけが存在する可能性がありますが、プロファイルに常に存在する保証はありません。 Outlookに正常に接続するまで、どちらのプロパティにも書き込Exchange Server。 
  
Outlook オブジェクト モデルでは **、NameSpace** オブジェクトの **ExchangeMailboxServerVersion** プロパティを使用して、アクティブなメールボックスがホストされている Exchange Server のバージョンを検索できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
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

