---
title: '[オンライン] で UDF Excelを構成Office Online Server'
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
ms.localizationpriority: medium
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: カスタム関数を呼び出す場合は、Excelのユーザー Office Online Server関数 (UDF) を使用します。
ms.openlocfilehash: caaf2eb4d0be74423759eaa25bb6499a0350006f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601388"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>[オンライン] で UDF Excelを構成Office Online Server

カスタム関数を呼び出す場合は、Excelのユーザー Office Online Server関数 (UDF) を使用します。 
  
Excel Online でユーザー定義関数 (UDF) を使用すると、セル内の数式を使用して、マネージ コードで記述されたカスタム関数を呼び出すことができます。UDF は、次の目的で使用できます。
  
- カスタムの数学関数を呼び出す
    
- カスタム データ ソースからデータを取得してワークシートに入力する
    
- Web サービスを呼び出す
    
UDF バイナリは、以下の 2 つの場所のいずれかにインストールできます。
  
- ローカル ディレクトリ。例: 
    
    C:\UDFs\MySampleUdf.dll
    
- グローバル アセンブリ キャッシュ。例: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
新しい **OfficeWebAppsExcelUserDefinedFunction** 定義を作成するときに場所を参照Office Online Server。 
  
> [!NOTE]
> Office Online Server共有上にある UDF はサポートされていません。 
  
## <a name="enable-udfs-on-office-online-server"></a>デバイスで UDF を有効Office Online Server 

管理者が[New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps)コマンドレットOfficeして Web Apps Server ファームに新しいアプリケーション をWindows PowerShellすると、UDF アセンブリは既定で無効になっています。 **ExcelUdfsAllowed** フラグの既定値は false です。 
  
UDF を有効にするには、Web Apps サーバー ファームWindows PowerShellした後、Office Online Serverで次Officeコマンドを実行します。
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>UDF 定義を作成するOffice Online Server

UDF を有効にした後に、UDF を含むバイナリの定義を作成する必要があります。 UDF バイナリの定義を作成するには、Office Online Server **New-OfficeWebAppsExcelUserDefinedFunction コマンドレットを使用** します。 このコマンドレットには、次のパラメーターが含まれます。 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Enable** (既定で False に設定されます) 
    
- **説明**
    
次の例は、UDF 定義を作成する方法を示しています。
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
新しい UDF 参照を作成した後、サーバーで **iisreset** を実行して、その参照をすぐに選択します。 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>UDF Office Online ServerコマンドWindows PowerShell追加

UDF を使用するにはWindows PowerShellのコマンドレットを使用します。
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (必須パラメーターなし) - アプリケーションで構成されている UDF 定義の一覧をOffice Online Server。 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義にプロパティを設定します。 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義を削除します。 
    
## <a name="udf-sample"></a>UDF のサンプル

次のサンプル ファイルは、UDF と UDF バイナリを使用するサンプル ブックを提供します。
  
- [BooleanDataType.xlsx: ](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx)UDF を使用するサンプル ブック  
    
## <a name="see-also"></a>関連項目

- [Excel Online の管理設定を行う](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

