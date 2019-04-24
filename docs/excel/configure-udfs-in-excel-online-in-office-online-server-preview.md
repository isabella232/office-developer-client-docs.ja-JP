---
title: Office online Server の Excel Online で udf を構成する
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Office online Server の Excel online でユーザー定義関数 (udf) を使用して、カスタム関数を呼び出します。
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311061"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Office online Server の Excel Online で udf を構成する

Office online Server の Excel online でユーザー定義関数 (udf) を使用して、カスタム関数を呼び出します。 
  
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
> Office Online Server は、ネットワーク共有にある udf をサポートしていません。 
  
## <a name="enable-udfs-on-office-online-server"></a>Office Online Server で udf を有効にする 

管理者が、 [new-officewebappsfarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell コマンドレットを使用して新しい Office Web Apps サーバーファームを作成する場合、UDF アセンブリは既定で無効になっています。 **ExcelUdfsAllowed** フラグの既定値は false です。 
  
udf を有効にするには、office Web Apps サーバーファームが作成された後、office Online server で次の Windows PowerShell コマンドを実行します。
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Office Online Server で UDF 定義を作成する

UDF を有効にした後に、UDF を含むバイナリの定義を作成する必要があります。 Office Online Server で UDF バイナリの定義を作成するには、 **OfficeWebAppsExcelUserDefinedFunction**コマンドレットを使用します。 このコマンドレットには、次のパラメーターが含まれます。 
  
- **アセンブリ**
    
- **assemblylocation**
    
- **Enable** (既定で False に設定されます) 
    
- **説明**
    
次の例は、UDF 定義を作成する方法を示しています。
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
新しい UDF 参照を作成した後、サーバーで **iisreset** を実行して、その参照をすぐに選択します。 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>その他の Office Online Server UDF の Windows PowerShell コマンド

udf を操作するには、次の Windows PowerShell コマンドレットを使用します。
  
- **OfficeWebAppsExcelUserDefinedFunction**(必須のパラメーターはありません)-Office Online Server で構成されている UDF 定義の一覧を返します。 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義にプロパティを設定します。 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義を削除します。 
    
## <a name="udf-sample"></a>UDF のサンプル

次のファイルは、UDF と UDF バイナリを使用するサンプルのブックを提供します。
  
- [BooleanDataType](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): UDF を使用するサンプルブック  
- [EcsUdfsCommonSet](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): UDF バイナリ 
    
## <a name="see-also"></a>関連項目

- [Excel Online の管理設定を行う](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

