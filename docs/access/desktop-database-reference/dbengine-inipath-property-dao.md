---
title: DBEngine.IniPath プロパティ (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a84c27407ee370c406f791fa691d30fda3e79810
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585803"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath プロパティ (DAO)


**適用先**: Access 2013、Office 2013

Microsoft Access データベース エンジン用の値が含まれた Windows レジストリ キーに関する情報を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .IniPath

*式* **DBEngine** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

Microsoft Access データベース エンジンは、レジストリを使用してWindowsできます。 このレジストリを使用すると、インストール可能な ISAM DLL などのオプションを設定できます。

このオプションを有効にするには、 **IniPath** プロパティを設定してから、アプリケーションで他の DAO コードを呼び出す必要があります。この設定の有効範囲は使用するアプリケーションに限定され、範囲を変更するにはアプリケーションを再起動する必要があります。

また、レジストリを使用すると、インストール可能な ISAM データベース ドライバーの初期化パラメーターを用意できます。たとえば、Paradox バージョン 4.0 を使用するには、 **IniPath** プロパティを、該当するパラメーターが含まれたレジストリの一部の値に設定します。

このプロパティは、HKEY \_ LOCAL \_ MACHINE または HKEY LOCAL USER のいずれかを \_ 認識 \_ します。 ルート キーが指定されていない場合、既定値は HKEY \_ LOCAL \_ MACHINE です。

