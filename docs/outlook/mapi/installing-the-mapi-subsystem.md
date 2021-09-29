---
title: MAPI サブシステムのインストール
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: '最終更新日: 2015 年 3 月 9 日'
ms.localizationpriority: high
ms.openlocfilehash: 56aac9386076974cb0bb532af349c7b4243cbdcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630510"
---
# <a name="installing-the-mapi-subsystem"></a>MAPI サブシステムのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サポートされているバージョンの Windows で、_\<drive\>_ \Windows\System32 フォルダーに MAPI スタブ ライブラリ、Mapi32.dll をインストールします。 
  
サポートされているバージョンの Windows を次に示します。
  
- Windows 7。
    
- Windows Vista。
    
- Windows Server 2008。
    
- Windows Server 2003。
    
- Windows XP。
    
MAPI サブシステムを正しくインストールするには、MAPI ベースのサブシステム (Microsoft Outlook など) を含むアプリケーションをインストールします。
  
コンピューターの MAPI サブシステムのインストールに関する情報は、システム レジストリにあります。 レジストリ エントリの値は、すべて文字列です。 
  
メッセージ サービスのインストール プログラムは、次のシステム レジストリキーにインストール情報を作成します。 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
メッセージ サービスは、システム レジストリにエントリを追加する必要があります。 
  
次の表に、クライアントがコンピューター上の MAPI サブシステムのバージョン情報を取得する方法を要約します。
  
|**確認**|**レジストリ**|
|:-----|:-----|
|MAPI の可用性  <br/> |`MAPIX=1` を検索します。  <br/> |
|利用可能な MAPI のバージョン  <br/> |" _x.x.x_" 形式の MAPIXVER 文字列を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI プログラミングの概要](mapi-programming-overview.md)

