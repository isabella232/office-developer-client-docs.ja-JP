---
title: Office Online Server の Excel Online で Udf を構成する
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Office Online Server の Excel Online でユーザー定義関数 (Udf) を使用して、カスタム関数を呼び出します。
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102934"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Office Online Server の Excel Online で Udf を構成する

Office Online Server の Excel Online でユーザー定義関数 (Udf) を使用して、カスタム関数を呼び出します。 
  
Excel Online でユーザー定義関数 (UDF) を使用すると、セル内の数式を使用して、マネージ コードで記述されたカスタム関数を呼び出すことができます。UDF は、次の目的で使用できます。
  
- カスタムの数学関数を呼び出す
    
- カスタム データ ソースからデータを取得してワークシートに入力する
    
- Web サービスを呼び出す
    
UDF バイナリは、以下の 2 つの場所のいずれかにインストールできます。
  
- ローカル ディレクトリ。例: 
    
    C:\UDFs\MySampleUdf.dll
    
- グローバル アセンブリ キャッシュ。例: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Office Online Server で**OfficeWebAppsExcelUserDefinedFunction**定義を作成するときに場所を参照します。 
  
> [!NOTE]
> Office Online Server は、ネットワーク共有にある Udf をサポートしていません。 
  
## <a name="enable-udfs-on-office-online-server"></a>Office Online Server で Udf を有効にする 

管理者が、 [New-officewebappsfarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell コマンドレットを使用して新しい Office Web Apps サーバーファームを作成する場合、UDF アセンブリは既定で無効になっています。 **ExcelUdfsAllowed** フラグの既定値は false です。 
  
Udf を有効にするには、office Web Apps サーバーファームが作成された後、Office Online Server で次の Windows PowerShell コマンドを実行します。
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Office Online Server で UDF 定義を作成する

UDF を有効にした後に、UDF を含むバイナリの定義を作成する必要があります。 Office Online Server で UDF バイナリの定義を作成するには、 **OfficeWebAppsExcelUserDefinedFunction**コマンドレットを使用します。 このコマンドレットには、次のパラメーターが含まれます。 
  
- **アセンブリ**
    
- **AssemblyLocation**
    
- **Enable** (既定で False に設定されます) 
    
- **説明**
    
次の例は、UDF 定義を作成する方法を示しています。
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
新しい UDF 参照を作成した後、サーバーで **iisreset** を実行して、その参照をすぐに選択します。 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>その他の Office Online Server UDF の Windows PowerShell コマンド

Udf を操作するには、次の Windows PowerShell コマンドレットを使用します。
  
- **OfficeWebAppsExcelUserDefinedFunction** (必須のパラメーターはありません)-Office Online Server で構成されている UDF 定義の一覧を返します。 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義にプロパティを設定します。 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義を削除します。 
    
## <a name="udf-sample"></a>UDF のサンプル

次のサンプルファイルは、UDF と UDF バイナリを使用するサンプルブックを提供しています。
  
- [BooleanDataType](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): UDF を使用するサンプルブック  
    
## <a name="see-also"></a>関連項目

- [Excel Online の管理設定を行う](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

