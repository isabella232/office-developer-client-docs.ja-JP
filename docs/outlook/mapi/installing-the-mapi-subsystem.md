---
title: MAPI サブシステムのインストール
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: adb4d09ccce95683ac46e7b271fafa328b1a9f97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575351"
---
# <a name="installing-the-mapi-subsystem"></a>MAPI サブシステムのインストール

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サポートされているバージョンの Windows で Mapi32.dll、MAPI スタブ ライブラリをインストールする、_\<ドライブ\>_ \Windows\System32 フォルダーです。 
  
サポートされているバージョンの Windows は次のとおりです。
  
- Windows 7。
    
- Windows Vista の場合です。
    
- Windows Server 2008。
    
- Windows Server 2003 です。
    
- Windows XP です。
    
MAPI のサブシステムを正しくインストールするには、Microsoft Outlook などの MAPI ベースのサブシステムを含むアプリケーションをインストールします。
  
システム レジストリで、コンピューターの MAPI サブシステムのインストールに関する情報が表示されます。 レジストリ エントリのすべての値は、文字の文字列です。 
  
メッセージ サービスのインストール プログラムは、システムの次のレジストリ キーのインストール情報の作成を担当します。 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
メッセージ サービスは、システム レジストリにエントリを追加する必要があります。 
  
次の表は、クライアントが自分のコンピューター上の MAPI サブシステムのバージョン情報を取得する方法をまとめたものです。
  
|**チェックするには**|**Registry**|
|:-----|:-----|
|MAPI の可用性  <br/> |`MAPIX=1`。  <br/> |
|MAPI のバージョン  <br/> |" _X.x.x_"の形式の MAPIXVER 文字列を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI �v���O���~���O�̊T�v](mapi-programming-overview.md)

