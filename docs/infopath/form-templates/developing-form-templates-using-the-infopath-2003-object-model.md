---
title: InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを開発する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], using infopath 2003 object model,InfoPath 2003-compatible form templates,InfoPath 2007, developing form templates using InfoPath 2003 object model,object models [InfoPath 2003], developing managed code form templates
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Microsoft InfoPath は引き続き、Microsoft Office InfoPath 2003 Toolkit for Visual Studio .NET または Visual Studio 2005 Tools for the Microsoft Office system で作成され、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間のメンバーに対して書かれたビジネス ロジックを持つ、フォーム テンプレート プロジェクトをサポートします。このセクションのトピックでは、この名前空間の型とメンバーを InfoPath 2003 互換オブジェクト モデル、または単に InfoPath 2003 オブジェクト モデルと呼びます。InfoPath は、InfoPath 2003 互換オブジェクト モデルを使用する Microsoft Office InfoPath 2007 で作成されたフォーム テンプレート プロジェクトもサポートします。さらに、Office InfoPath 2007 のユーザー向けに下位互換性を維持するため、InfoPath を使用して、InfoPath 2003 互換オブジェクト モデルを使用する新しいフォーム テンプレート プロジェクトを作成できます。このセクションのトピックには、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルで動作するフォーム テンプレートの作成と開発に固有の情報が記載されています。
ms.openlocfilehash: 5d949242068586c752e7a92fa53792cda9ececea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799096"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを開発する

Microsoft InfoPath は引き続き、Microsoft Office InfoPath 2003 Toolkit for Visual Studio .NET または Visual Studio 2005 Tools for the Microsoft Office system で作成され、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間のメンバーに対して書かれたビジネス ロジックを持つ、フォーム テンプレート プロジェクトをサポートします。このセクションのトピックでは、この名前空間の型とメンバーを InfoPath 2003 互換オブジェクト モデル、または単に InfoPath 2003 オブジェクト モデルと呼びます。InfoPath は、InfoPath 2003 互換オブジェクト モデルを使用する Microsoft Office InfoPath 2007 で作成されたフォーム テンプレート プロジェクトもサポートします。さらに、Office InfoPath 2007 のユーザー向けに下位互換性を維持するため、InfoPath を使用して、InfoPath 2003 互換オブジェクト モデルを使用する新しいフォーム テンプレート プロジェクトを作成できます。このセクションのトピックには、 [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルで動作するフォーム テンプレートの作成と開発に固有の情報が記載されています。 
  
> [!IMPORTANT]
> [!重要] [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によって提供されるマネージ コード オブジェクト モデルを使用したビジネス ロジックの作成は今も InfoPath でサポートされていますが、このオブジェクト モデルを使用して書かれたビジネス ロジックは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 に展開されたブラウザー対応のフォーム テンプレートではサポートされていません。ブラウザー対応フォーム テンプレートは、カスタム ビジネス ロジック用に、 [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーによって提供される新しい InfoPath マネージ コード オブジェクト モデルを使用する必要があります。 [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーを使用して書かれたビジネス ロジックでフォーム テンプレートを作成する方法の詳細については、「 [コードを含む InfoPath フォーム テンプレートを開発する](developing-infopath-form-templates-with-code.md)」を参照してください。 > Visual Studio 2012 でコンパイルされたフォーム テンプレートのユーザーのコンピューターには、Microsoft .NET Framework 2.0 またはそれ以降がインストールされている必要があります。Visual Studio .NET 2003 でコンパイルされたフォーム テンプレートのユーザーのコンピューターには、Microsoft .NET Framework 1.1 があればかまいません。 
  
## <a name="in-this-section"></a>このセクションの内容

[InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートの開発作業を開始する](get-started-developing-form-templates-using-infopath-object-model.md)
  
> InfoPath 2003 互換オブジェクト モデルで動作するマネージ コード フォーム テンプレートの作成を開始する方法に関する情報を提供します。
    
[InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> 初期化とクリーンアップ コード、イベント ハンドラーの追加方法、マネージ コード フォーム テンプレートのデバッグと展開方法、スレッドのサポート、および InfoPath マネージ コード ソリューションから Microsoft XML Core Services (MSXML) で作業する方法について説明します。
    
[コードを含む InfoPath フォーム テンプレートのセキュリティ](security-in-infopath-form-templates-with-code.md)
  
> マネージ コードを使用した InfoPath フォーム テンプレートのセキュリティ モデル、完全に信頼された InfoPath フォーム テンプレートのデバッグ、および関連するセキュリティ手順について説明します。
    
[InfoPath 2003 オブジェクト モデルを理解する](understanding-the-infopath-2003-object-model.md)
  
> InfoPath 2003 互換オブジェクト モデル、およびそのオブジェクト モデルで動作するマネージ コード フォーム テンプレートのプログラミングでよく行う作業について説明します。
    
[InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートをトラブルシューティングする](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> InfoPath 2003 互換オブジェクト モデルで動作するマネージ コード フォーム テンプレートを作成する際に発生する可能性のある一般的な問題の解決に役立つヒントが記載されています。
    
## <a name="related-sections"></a>関連セクション

[InfoPath デベロッパー ポータル](http://go.microsoft.com/fwlink?LinkID=11689)
  
> カスタム InfoPath ソリューションの構築に関する技術的な記事、コード サンプル、ダウンロード、サポート、およびその他の MSDN ドキュメントが含まれています。
    
[Microsoft Office デベロッパー センター](http://go.microsoft.com/fwlink?LinkID=27128)
  
> カスタム Office ソリューションの構築に関する技術的な記事、コード サンプル、ダウンロード、サポート、およびその他の MSDN ドキュメントへのリンクが含まれています。
    

