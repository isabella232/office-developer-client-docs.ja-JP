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
ms.openlocfilehash: 99e2b31cf686895a56e9d70b177314355c1aff3c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945147"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="fb861-102">Microsoft Access データベース エンジン用の Windows レジストリ設定のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="fb861-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="fb861-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fb861-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb861-104">アプリケーションは、Microsoft Access データベース エンジンの既定の機能で正常に動作することはできません、する場合は、お客様のニーズに合わせて Microsoft Windows レジストリの設定を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb861-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="fb861-105">また、Windows レジストリを使用して、組み込み可能な ISAM ドライバーと ODBC ドライバーの動作を調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="fb861-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="fb861-106">Windows レジストリの設定は、次の 4 とおりの方法でカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="fb861-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- <span data-ttu-id="fb861-107">[Regedit.exe を使用して既定の設定を上書きするには](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="fb861-107">[Using Regedit.exe to overwrite the default settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>
- <span data-ttu-id="fb861-108">[設定を管理するのには、アプリケーションのレジストリ ツリーの一部を作成します。](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="fb861-108">[Creating a portion in your application's registry tree to manage the settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>
- <span data-ttu-id="fb861-109">[DAO から SetOption メソッドを使用します。](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="fb861-109">[Using the SetOption method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>
- <span data-ttu-id="fb861-110">[アクセス用の Microsoft OLE DB プロバイダーの接続プロパティを使用してください。](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="fb861-110">[Using the Connection properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

