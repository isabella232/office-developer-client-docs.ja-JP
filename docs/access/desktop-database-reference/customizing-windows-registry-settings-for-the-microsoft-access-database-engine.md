---
title: Microsoft Access データベース エンジン用の Windows レジストリ設定のカスタマイズ
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b961869f3add04cf4af827f96721aad6dba611b6
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025603"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="fb0dc-102">Microsoft Access データベース エンジン用の Windows レジストリ設定のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="fb0dc-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="fb0dc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fb0dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb0dc-104">アプリケーションは、Microsoft Access データベース エンジンの既定の機能で正常に動作することはできません、する場合は、お客様のニーズに合わせて Microsoft Windows レジストリの設定を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb0dc-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="fb0dc-105">また、Windows レジストリを使用して、組み込み可能な ISAM ドライバーと ODBC ドライバーの動作を調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="fb0dc-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="fb0dc-106">Windows レジストリの設定は、次の 4 とおりの方法でカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="fb0dc-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- [<span data-ttu-id="fb0dc-107">Regedit.exe を使用して既定の設定を上書きするには</span><span class="sxs-lookup"><span data-stu-id="fb0dc-107">Using Regedit.exe to overwrite the default settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [<span data-ttu-id="fb0dc-108">設定を管理するのには、アプリケーションのレジストリ ツリーの一部を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb0dc-108">Creating a portion in your application's registry tree to manage the settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [<span data-ttu-id="fb0dc-109">DAO から SetOption メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb0dc-109">Using the SetOption method from DAO</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [<span data-ttu-id="fb0dc-110">アクセス用の Microsoft OLE DB プロバイダーの接続プロパティを使用してください。</span><span class="sxs-lookup"><span data-stu-id="fb0dc-110">Using the Connection properties in the Microsoft OLE DB Provider for Access</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

