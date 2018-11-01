---
title: Microsoft Access データベース エンジンの Windows レジストリ設定をカスタマイズします。
TOCTitle: Customizing Windows Registry Settings for the Microsoft Access Database Engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a44226e8ea90a8be96de35cdc923349eded17cb4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886999"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="62e02-102">Microsoft Access データベース エンジン用の Windows レジストリ設定をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="62e02-102">Customizing Windows Registry Settings for the Microsoft Access Database Engine</span></span>


<span data-ttu-id="62e02-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="62e02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62e02-p101">アプリケーションで Microsoft Access データベース エンジンの既定の機能が正常に動作しない場合は、必要に応じて Microsoft® Windows® レジストリの設定を変更しなければなりません。また、Windows レジストリを使用して、組み込み可能な ISAM ドライバーと ODBC ドライバーの動作を調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="62e02-p101">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft® Windows® Registry to suit your needs. The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="62e02-106">Windows レジストリの設定は、次の 4 とおりの方法でカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="62e02-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

<span data-ttu-id="62e02-107">[Regedit.exe を使用して既定の設定を上書きする](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="62e02-107">[Using Regedit.exe to Overwrite the Default Settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>

<span data-ttu-id="62e02-108">[設定を管理するための部分をアプリケーションのレジストリ ツリーに作成する ](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="62e02-108">[Creating a Portion in Your Application's Registry Tree to Manage the Settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>

<span data-ttu-id="62e02-109">[DAO から SetOption メソッドを使用する](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="62e02-109">[Using the SetOption Method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>

<span data-ttu-id="62e02-110">[Microsoft OLE DB Provider for Access で接続プロパティを使用する](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="62e02-110">[Using the Connection Properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

