---
title: PidTagProfileHomeServerFQDN 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b02a55f7b87bef6a4304d006f79472bcf21c811e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581875"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>PidTagProfileHomeServerFQDN 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイル構成の Kerberos 認証を有効にします。
  
****

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|識別子:  <br/> |0x662A001F  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>注釈

により直接接続するドメイン コント ローラー (DC)、Microsoft Exchange Server 2007 に対して Kerberos 認証を使用するように構成されたプロファイルに必要なユーザーのディレクトリ サーバーのドメイン名にこのプロパティを設定し、以前のバージョンで**PR_PROFILE_AUTH_PACKAGE**で**RPC_C_AUTHN_GSS_KERBEROS**を設定します。
  
> [!NOTE]
> Microsoft Exchange Server 2010 と Exchange Server 2013 は、アドレス帳からの呼び出しをクライアント アクセス サーバーとは異なるで Exchange Server 2007 と以前のバージョンを処理する方法を処理します。 DSProxy プロセスは使用されませんので、Kerberos 認証が成功することがあります。 ただし、クライアントがあると通信できている Exchange サーバーの代わりに直接、DC では、適さない場合があります: 設定**PR_PROFILE_HOME_SERVER_FQDN**がこれを回避できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コア メッセージのストア オブジェクトの許可された操作を指定します。
    
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

