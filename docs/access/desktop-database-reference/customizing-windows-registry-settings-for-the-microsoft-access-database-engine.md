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
localization_priority: Normal
ms.openlocfilehash: 7cbe8ad56e01249563f7b06c9018d923a96246e9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707361"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Microsoft Access データベース エンジン用の Windows レジストリ設定のカスタマイズ

**適用されます**Access 2013、Office 2013。

アプリケーションは、Microsoft Access データベース エンジンの既定の機能で正常に動作することはできません、する場合は、お客様のニーズに合わせて Microsoft Windows レジストリの設定を変更する必要があります。 また、Windows レジストリを使用して、組み込み可能な ISAM ドライバーと ODBC ドライバーの動作を調整することもできます。

Windows レジストリの設定は、次の 4 とおりの方法でカスタマイズできます。

- [Regedit.exe を使用して既定の設定を上書きするには](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [設定を管理するのには、アプリケーションのレジストリ ツリーの一部を作成します。](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [DAO から SetOption メソッドを使用します。](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [アクセス用の Microsoft OLE DB プロバイダーの接続プロパティを使用してください。](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

