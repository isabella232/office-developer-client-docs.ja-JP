---
title: IniPath プロパティ (DAO)
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
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294296"
---
# <a name="dbengineinipath-property-dao"></a>IniPath プロパティ (DAO)


**適用先:** Access 2013、Office 2013

Microsoft Access データベース エンジン用の値が含まれた Windows レジストリ キーに関する情報を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*。IniPath

*式***DBEngine**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

Windows レジストリを使用して、Microsoft access データベースエンジンを構成できます。 このレジストリを使用すると、インストール可能な ISAM DLL などのオプションを設定できます。

このオプションを有効にするには、 **IniPath** プロパティを設定してから、アプリケーションで他の DAO コードを呼び出す必要があります。この設定の有効範囲は使用するアプリケーションに限定され、範囲を変更するにはアプリケーションを再起動する必要があります。

また、レジストリを使用すると、インストール可能な ISAM データベース ドライバーの初期化パラメーターを用意できます。たとえば、Paradox バージョン 4.0 を使用するには、 **IniPath** プロパティを、該当するパラメーターが含まれたレジストリの一部の値に設定します。

このプロパティは、hkey\_ローカル\_コンピューターまたは\_hkey\_ローカルユーザーのいずれかを認識します。 ルートキーが指定されていない場合、\_既定\_値は HKEY ローカルコンピューターになります。

