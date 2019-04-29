---
title: SharePoint オブジェクト モデルのメンバーを使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: InfoPath フォーム テンプレート内で実行されるコードから、SharePoint オブジェクト モデルのメンバーに対してプログラミングを行う場合は、事前に、フォームの Visual Studio 2012 プロジェクトで Microsoft.SharePoint.dll アセンブリを参照する必要があります。そのためには、Microsoft SharePoint Server 2010 のライセンス コピーのファイル システム、または Microsoft SharePoint Foundation 2010 を実行するサーバーのファイル システムにアクセスして、Microsoft.SharePoint.dll アセンブリのコピーを取得する必要があります。
ms.openlocfilehash: e29725450a6a1bdcba99215e337493f8686491e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431660"
---
# <a name="use-sharepoint-object-model-members"></a>SharePoint オブジェクト モデルのメンバーを使用する

InfoPath フォーム テンプレート内で実行されるコードから、SharePoint オブジェクト モデルのメンバーに対してプログラミングを行う場合は、事前に、フォームの Visual Studio 2012 プロジェクトで Microsoft.SharePoint.dll アセンブリを参照する必要があります。そのためには、Microsoft SharePoint Server 2010 のライセンス コピーのファイル システム、または Microsoft SharePoint Foundation 2010 を実行するサーバーのファイル システムにアクセスして、Microsoft.SharePoint.dll アセンブリのコピーを取得する必要があります。 
  
また、フォーム テンプレートを、サンドボックス ソリューションまたは管理者承認ソリューションのどちらかとして、サーバーに展開する必要もあります。これらの展開オプションの詳細については、「[コードを含むフォームを発行する](publishing-forms-with-code.md)」を参照してください。
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Microsoft.SharePoint アセンブリを追加して、InfoPath フォーム テンプレートから参照する

> [!IMPORTANT]
> InfoPath プロジェクト システムがフォーム テンプレート ファイルに追加されるファイルを管理する方法と競合しないように、フォーム テンプレート プロジェクトの最上位フォルダーには、参照するアセンブリをコピーしないでください。既定では、このフォルダーのパス形式は、< *ドライブ*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *製品名*  となります。 > 参照するアセンブリをプロジェクト フォルダー内で移動するには、メインの *製品名*  プロジェクト フォルダーの下にサブフォルダーを作成し、そのサブフォルダーにコピーしたアセンブリを参照する必要があります。ただし、参照するアセンブリのためのサブフォルダーを作成する必要はありません。参照するアセンブリがプロジェクトの最上位フォルダーになければ、プロジェクトをコンパイルおよび発行したときに、InfoPath プロジェクト システムによってアセンブリがフォーム テンプレート ファイル (.xsn) にコピーされます。 
  
既定では、Microsoft.SharePoint.Server.dll は、SharePoint Server 2010 のファイル システム、または SharePoint Foundation 2010 を実行するサーバーのファイル システムの C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI にインストールされます。
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>Microsoft.SharePoint アセンブリを、InfoPath フォームのコード プロジェクトから参照するには

1. Microsoft.SharePoint.Server.dll アセンブリをサーバーからローカル フォルダーにコピーするか、共有フォルダーからアセンブリへのアクセスを取得します。
    
2. Visual Studio 2012 で、フォーム テンプレート プロジェクトを開きます。
    
3. [ **プロジェクト**] メニューの [ **参照の追加**] をクリックします。
    
4. [ **参照**] タブをクリックし、アセンブリを探して選択し、[ **OK**] をクリックして参照を追加します。 
    
これで、SharePoint オブジェクト モデルのメンバーに対して、フォーム コードからコードを記述できるようになりました。Microsoft.SharePoint 名前空間のメンバーをより簡単に参照するには、コード ファイルの一番上のディレクティブに、 `using Microsoft.SharePoint;` または  `Imports Microsoft.SharePoint` を追加します。InfoPath フォーム内での SharePoint オブジェクト モデルのメンバーの使用例については、「 [サンドボックス ソリューションのサンプル](sample-sandboxed-solutions.md)」の「例 2: SharePoint リストでのベンダーの管理」を参照してください。

