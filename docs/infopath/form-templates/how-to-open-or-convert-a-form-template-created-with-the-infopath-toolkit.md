---
title: InfoPath Toolkit で作成したフォーム テンプレートを開くか変換する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- converting form templates [infopath 2007],InfoPath Toolkit, opening form templates from,form templates [InfoPath 2007], opening,InfoPath 2007, converting InfoPath Toolkit form templates,opening form templates [InfoPath 2007],form templates [InfoPath 2007], converting,script [InfoPath 2007], converting to managed code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: InfoPath 2003 Toolkit for Visual Studio に含まれるツールキットを使用して InfoPath 2003 マネージ コード フォーム テンプレートを作成した場合に、InfoPath 2003 との互換性を維持するには、Microsoft InfoPath および Visual Studio 2012 でフォーム テンプレート プロジェクト開きます。これにより、引き続きそのフォーム テンプレート プロジェクトを使用して開発を進めることができます。
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428586"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>InfoPath Toolkit で作成したフォーム テンプレートを開くか変換する

InfoPath 2003 Toolkit for Visual Studio に含まれるツールキットを使用して InfoPath 2003 マネージ コード フォーム テンプレートを作成した場合に、InfoPath 2003 との互換性を維持するには、Microsoft InfoPath および Visual Studio 2012 でフォーム テンプレート プロジェクト開きます。これにより、引き続きそのフォーム テンプレート プロジェクトを使用して開発を進めることができます。
  
または、InfoPath 2003 プロジェクトのコードを移行およびアップグレードして、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される新しい .NET オブジェクト モデルを使用することもできます。その場合は、 **Microsoft.Office.InfoPath** 名前空間のメンバーを使用するようにすべてのコードを書き直す必要があります。ただし、以前のプロジェクトのコードはすべて、 **#if InfoPathManagedObjectModel** ステートメントと **#endif** ステートメント (C# の場合) または **#If InfoPathManagedObject Model** ステートメントと **#End If** ステートメント (Visual Basic の場合) で囲まれて、参照用に維持されます。 
  
以下の手順では、InfoPath Toolkit を使用して作成したマネージ コード フォーム テンプレートを開いて InfoPath 2003 との互換性を維持する方法と、新しい InfoPath オブジェクト モデルに移行およびアップグレードする方法を説明します。 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>InfoPath Toolkit で作成したマネージ コード フォーム テンプレートを Visual Studio Tools for Applications を使用して開き、InfoPath 2003 との互換性を維持する

1. InfoPath デザイン モードを開き、[ **ファイル**] タブの [ **開く**] をクリックします。 
    
2. [ **デザイン モードで開く**] ダイアログ ボックスで、InfoPath Toolkit フォーム テンプレート プロジェクトが保存されているプロジェクト フォルダーに移動します。 
    
    By default, this will be a folder in  `C:\Users\` *username*  `\Documents\Visual Studio Projects` on the computer where the project was created. Or, you can move the folder to the location where InfoPath stores Visual Studio 2012 projects, which by default is  `C:\Users\` *username*  `\Documents\InfoPath Projects`
    
3. manifest.xsf という名前のファイルをクリックし、[ **開く**] をクリックします。
    
4. [ **開発**] タブの [ **コード エディター**] をクリックします。
    
5. "Visual Basic または Visual C# コードを追加する前に、このフォーム テンプレートを保存する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。 
    
6. ファイルを保存する場所に移動し、ファイルの名前を入力して、[ **保存**] をクリックします。
    
7. "このコードは InfoPath 2003 Toolkit for Microsoft Visual Studio に含まれるツールキットで作成されたものです。InfoPath では、このツールキット プロジェクトを新しい形式に移行する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。 
    
8. プロジェクトの Visual Studio ソリューション (.sln) ファイルを選択し、[ **開く**] をクリックします。
    
9. 移行プロセスが完了すると、"プロジェクトが移行されました" というメッセージが表示されます。[ **OK**] をクリックして続行します。 
    
10. "このフォームのコードは、InfoPath 2003 オブジェクト モデルを使用しています" というメッセージが表示され、"Microsoft Office InfoPath オブジェクト モデルを使用するようにコードをアップグレードしますか?" とたずねられます。InfoPath 2003 との互換性を維持し、**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを引き続き使用するには、[ [いいえ](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)] をクリックします。 
    
    InfoPath 2003 と互換性のあるマネージ コード フォーム テンプレートの作業方法の詳細については、「[InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを開発する](developing-form-templates-using-the-infopath-2003-object-model.md)」を参照してください。
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>InfoPath Toolkit で作成したマネージ コード フォーム テンプレートを Visual Studio Tools for Applications を使用して開き、新しい InfoPath オブジェクト モデルを使用するようにアップグレードする

1. InfoPath デザイン モードを開き、[ **ファイル**] タブの [ **開く**] をクリックします。 
    
2. [ **フォーム テンプレートを開く**] で、[ **自分のコンピューター上**] をクリックします。
    
3. [ **デザイン モードで開く**] ダイアログ ボックスで、InfoPath Toolkit フォーム テンプレート プロジェクトが保存されているプロジェクト フォルダーに移動します。 
    
    By default this will be a folder in  `C:\Users\` *username*  `\Documents\Visual Studio Projects` on the computer where the project was created. Or, you can move the folder to the location where InfoPath stores Visual Studio 2012 projects, which by default is  `C:\Users\` *username*  `\Documents\InfoPath Projects`
    
4. manifest.xsf という名前のファイルをクリックし、[ **開く**] をクリックします。
    
5. [ **開発**] タブの [ **コード エディター**] をクリックします。
    
6. "Visual Basic または Visual C# コードを追加する前に、このフォーム テンプレートを保存する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。 
    
7. ファイルを保存する場所に移動し、ファイルの名前を入力して、[ **保存**] をクリックします。
    
8. "このコードは InfoPath 2003 Toolkit for Microsoft Visual Studio に含まれるツールキットで作成されたものです。InfoPath では、このツールキット プロジェクトを新しい形式に移行する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。 
    
9. プロジェクトの Visual Studio ソリューション (.sln) ファイルを選択し、[ **開く**] をクリックします。
    
10. 移行プロセスが完了すると、"プロジェクトが移行されました" というメッセージが表示されます。[ **OK**] をクリックして続行します。 
    
11. "このフォームのコードは、InfoPath 2003 オブジェクト モデルを使用しています" というメッセージが表示され、"Microsoft Office InfoPath オブジェクト モデルを使用するようにコードをアップグレードしますか?" とたずねられます。[ **はい**] をクリックして、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される新しいマネージ コード オブジェクト モデルを使用するようにフォーム テンプレートをアップグレードします。 
    
    フォーム コードが Visual Studio 2012 コード エディターで開きます。以前のプロジェクトのすべてのコードが、 **#if** **InfoPathManagedObjectModel** ステートメントと **#endif** ステートメント (C# の場合) または **#If InfoPathManagedObjectModel** ステートメントと **#End If** ステートメント (Visual Basic の場合) で囲まれて、参照用に維持されています。これらすべてのコードを、 **Microsoft.Office.InfoPath** 名前空間によって提供されるオブジェクト モデルのメンバーを使用するように書き換える必要があります。 
    
    新しい InfoPath マネージ コード オブジェクト モデルを使用するマネージ コード フォーム テンプレートの作業方法の詳細については、「[コードを含む InfoPath フォーム テンプレートを開発する](developing-infopath-form-templates-with-code.md)」を参照してください。
    

