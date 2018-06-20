---
title: MAPI サブシステムをインストールします。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801070"
---
# <a name="installing-the-mapi-subsystem"></a>MAPI サブシステムをインストールします。

  
  
**適用されます**: Outlook 
  
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

