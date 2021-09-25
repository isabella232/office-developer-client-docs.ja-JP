---
title: 概要 - インデックス作成用のストアの登録
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e972c0a443a0c06b4df5cde5ea0ec82587d077b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588267"
---
# <a name="about-registering-stores-for-indexing"></a>概要 - インデックス作成用のストアの登録

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックは、2007 年のインスタント検索Microsoft Office Outlookです。
  
インスタント検索を使用すると、アプリ内のアイテムをすばやくOutlook。 デスクトップ検索のコンポーネントWindows使用します。
  
MAPI プロトコル ハンドラーは、検索Windowsインデックスを作成する必要があるストアのレジストリをチェックします。 インデックスを作成するストア プロバイダーは、レジストリに登録Windows必要があります。
  
既定では、Windowsデスクトップ検索は、インデックス作成を許可するために、次の 4 種類のストア プロバイダーを Windowsレジストリに追加します。
  
- 個人用フォルダー ファイルの保存 (.PST)。
    
-  Microsoft Exchange(オフライン フォルダー ファイル (.ost) を含む) を格納します。 
    
-  パブリック フォルダー用のストア。 
    
-  MSN 用Microsoft Office Outlookコネクタ用に格納します。 
    
 インデックスを作成するサード パーティのストア プロバイダーは、自身をレジストリに登録Windows必要があります。 
  
> [!NOTE]
> 管理者とユーザーは、グループ ポリシー設定を使用して、デスクトップWindowsアイテムのインデックスを作成Outlookできます。 詳細については[、「Extending Windows デスクトップ検索」を参照してください](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)。 
  
## <a name="registry-keys"></a>レジストリ キー

コンピューターでは、インデックスを作成するストア プロバイダーはすべて、次の 3 つのレジストリ キーの 1 つのみ登録する必要があります。Windowsします。 MAPI プロトコル ハンドラーは、これらの各キーの下を次の順序で確認します。
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows\Preferences\
    
 キーの下の各値は、インデックスが作成されるストア プロバイダーに対応します。 値の名前は、ストア プロバイダーのグローバル一意識別子 (GUID) です。これは **DWORD** 型で、値は 16 進値0x00000001。 
  
## <a name="guids-for-store-providers"></a>ストア プロバイダーの GUID

MAPI プロパティは **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** MAPI ストアの GUID を指定します。 インデックスを作成するストア プロバイダー Outlook、次の表で説明します。 
  
||||
|:-----|:-----|:-----|
|**ストア プロバイダーの種類** <br/> |**GUID** <br/> |**注** <br/> |
|個人用フォルダー ファイル (.PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID は、パブリック ヘッダー ファイル mspst.h に次のように **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID はパブリック ヘッダー ファイル edkmdb.h に **pbExchangeProviderPrimaryUserGuid として文書化されています** <br/> |
|パブリック フォルダー  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID はパブリック ヘッダー ファイル edkmdb.h に **pbExchangeProviderPublicGuid として文書化されています** <br/> |
|OutlookMSN 用コネクタ  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |なし  <br/> |
   
## <a name="see-also"></a>関連項目



[ストア API について](about-the-store-api.md)

