---
title: インデックス作成のためのストア登録について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321827"
---
# <a name="about-registering-stores-for-indexing"></a>インデックス作成のためのストア登録について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックは、Microsoft Office Outlook 2007 のクイック検索に固有のものです。
  
クイック検索を使用すると、Outlook のアイテムをすばやく見つけることができます。 Windows デスクトップサーチのコンポーネントを使用します。
  
MAPI プロトコルハンドラーは、検索用にインデックスが必要なストアの Windows レジストリをチェックします。 インデックスを作成するストアプロバイダーは、Windows レジストリに登録する必要があります。
  
既定では、windows デスクトップ検索は、次の4種類のストアプロバイダーを windows レジストリに追加して、インデックスを許可します。
  
- 個人用フォルダーファイルのストア (。PST)。
    
-  すべてのオフラインフォルダーファイル (.ost) を含む Microsoft Exchange ストア。 
    
-  パブリックフォルダーのストア。 
    
-  Microsoft Office Outlook Connector for MSN に保存します。 
    
 インデックスを作成するサードパーティ製のストアプロバイダーは、Windows レジストリに登録する必要があります。 
  
> [!NOTE]
> 管理者とユーザーは、グループポリシー設定を使用して、Windows デスクトップサーチが Outlook アイテムのインデックスを作成できないようにすることができます。 詳細については、「 [Windows デスクトップサーチの拡張](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)」を参照してください。 
  
## <a name="registry-keys"></a>レジストリキー

コンピューターでは、インデックスを作成するすべてのストアプロバイダーは、Windows レジストリ内の次の3つのレジストリキーのいずれか1つにのみ登録されている必要があります。 MAPI プロトコルハンドラーは、次の順序で各キーの下を調べます。
  
1. [HKLM] \Software\Policies\Microsoft\Windows\Windows Search \
    
2. [HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\
    
 キーの下の各値は、インデックスを作成するストアプロバイダーに対応しています。 値の名前は、格納プロバイダーのグローバル一意識別子 (GUID) です。これは、 **DWORD**型で、16進数の値0x00000001 です。 
  
## <a name="guids-for-store-providers"></a>ストアプロバイダーの guid

mapi プロパティ**[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** は、mapi ストアの GUID を指定します。 次の表では、Outlook インデックスが格納されているストアプロバイダーの guid について説明します。 
  
||||
|:-----|:-----|:-----|
|**ストアプロバイダーの種類** <br/> |**GUID** <br/> |**メモ** <br/> |
|個人用フォルダーファイル (。PST  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID は、 **MSPST_UID_PROVIDER**として、パブリックヘッダーファイル mspst に記載されています。 <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |guid は、パブリックヘッダーファイル edkmdb で、 **pbexchangeproviderprimaryuserguid**としてドキュメント化されています。 <br/> |
|パブリック フォルダー  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID は、パブリックヘッダーファイル edkmdb では**pbexchangeproviderpublicguid**として記述されています。 <br/> |
|MSN 用 Outlook コネクタ  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |なし  <br/> |
   
## <a name="see-also"></a>関連項目



[ストア API について](about-the-store-api.md)

