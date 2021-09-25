---
title: PidTagProfileServerVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 61e7e9071bf943320fcd41cbb933e00cd123907c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616426"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>PidTagProfileServerVersion 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft プロファイルのアカウントが接続されているMicrosoft Exchange Serverのバージョンに関する情報Outlook指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|識別子:  <br/> |0x661B  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>注釈

プロファイルは、1 つのアカウントに接続する 1 つ以上のアカウントをExchange Server、同じアカウントに接続する必要Exchange Server。
  
Outlook 2007 Microsoft Office Outlook より前のバージョンでは、このプロパティに書き込み、アクティブ なプロファイルが接続されている Exchange Server のバージョンに関する情報を格納できます。 ただし、バージョン情報の形式は、バージョンごとに異Exchange Server。 たとえば、Outlook は 2003 年のバージョン識別子 **6.5.6944.3** のメジャー ビルド番号のみを表す 10 進数の値 6944 を PR_PROFILE_SERVER_VERSION に格納Microsoft Exchange Serverします。  2007 Exchange 2007 接続の場合、Outlook はメジャー バージョン番号とメジャー ビルド番号を、これらの番号の連結された 16 進表記でプロパティに格納します。 2007 Exchange **8.0.685.24** のバージョン識別子には、メジャー バージョン番号 8 と 10 進数のメジャー ビルド番号 685 があります。 両方の数値を 16 進数に変換すると、0x8と0x2AD。 これら 2 つの数値を連結するとOutlook値が 16 進表記 **0x82ADにPR_PROFILE_SERVER_VERSION** 格納されます。 
  
Outlook 2007 は、このプロパティの読み取りまたは書き込みを行う必要があります。 これは、PR_PROFILE_SERVER_FULL_VERSION **[をサポートしています](pidtagprofileserverfullversion-canonical-property.md)**。 
  
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

