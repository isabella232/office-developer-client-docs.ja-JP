---
title: インデックス作成のためのストア登録について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386531"
---
# <a name="about-registering-stores-for-indexing"></a>インデックス作成のためのストア登録について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックは、Microsoft Office Outlook 2007 でクイック検索を特定します。
  
クイック検索では、Outlook でアイテムをすばやく検索することができます。 Windows デスクトップ サーチのコンポーネントを使用します。
  
MAPI プロトコル ハンドラーでは、検索用のストアにインデックスを作成するための Windows レジストリをチェックします。 インデックスを作成するストア プロバイダーは、Windows レジストリに登録しなければなりません。
  
既定では、Windows デスクトップ サーチのインデックス作成を許可する Windows レジストリに、ストア プロバイダーの次の 4 種類が追加されます。
  
- ストアの個人用フォルダー ファイル (。PST) です。
    
-  すべてのオフライン フォルダー ファイル (.ost) を含む、Microsoft Exchange ストアです。 
    
-  パブリック フォルダー ストアです。 
    
-  MSN の Microsoft Office Outlook のコネクタのストアです。 
    
 インデックスを作成するサード ・ パーティ製のストア プロバイダーは、Windows レジストリに自身を登録する必要があります。 
  
> [!NOTE]
> 管理者およびユーザーは、Windows デスクトップ サーチが Outlook アイテムのインデックスを作成することを防ぐため、グループ ポリシーの設定を使用できます。 詳細については、 [Windows デスクトップ サーチの拡張](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)を参照してください。 
  
## <a name="registry-keys"></a>レジストリ キー

コンピューターでは、Windows レジストリで次の 3 つのレジストリ キーの 1 つだけでインデックスを作成するすべてのストア プロバイダーを登録してください。 MAPI プロトコル ハンドラーは次の次の順序でこれらのキーの下にあります。
  
1. [HKLM] \Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\
    
 キーの下の各値は、ストア プロバイダーがインデックスを作成することに相当します。 値の名前は、グローバル一意識別子 (GUID) 0x00000001 の 16 進値には、 **DWORD**型のストア プロバイダーのです。 
  
## <a name="guids-for-store-providers"></a>ストア プロバイダーの Guid

**[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** の MAPI プロパティは、MAPI ストアの GUID を指定します。 Outlook のインデックスが次の表に記載されているストア プロバイダーの Guid です。 
  
||||
|:-----|:-----|:-----|
|**ストア プロバイダーの種類** <br/> |**GUID** <br/> |**メモ** <br/> |
|個人用フォルダー ファイル (。PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID が**MSPST_UID_PROVIDER**として、パブリック ヘッダー ファイル mspst.h に記載されています。 <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID が**pbExchangeProviderPrimaryUserGuid**として、パブリック ヘッダー ファイル edkmdb.h に記載されています。 <br/> |
|パブリック フォルダー  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID が**pbExchangeProviderPublicGuid**として、パブリック ヘッダー ファイル edkmdb.h に記載されています。 <br/> |
|の  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |なし  <br/> |
   
## <a name="see-also"></a>関連項目



[ストア API について](about-the-store-api.md)

