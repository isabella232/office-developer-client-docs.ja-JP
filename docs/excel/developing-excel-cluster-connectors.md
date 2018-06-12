---
title: Excel �N���X�^�[ �R�l�N�^�̊J��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798763"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="28d65-103">Excel �N���X�^�[ �R�l�N�^�̊J��</span><span class="sxs-lookup"><span data-stu-id="28d65-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="28d65-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="28d65-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="28d65-p101">Excel �N���X�^�[ �R�l�N�^�́AXLL ��̃N���X�^�[ �Z�[�t�̃��[�U�[��[](cluster-safe-functions.md)�֐��̏ڍׂɂ��ẮA�u[�N���X�^�[ �Z�[�t�֐�](cluster-safe-functions.md)�v��Q�Ƃ��Ă��������B���̃I�t���[�h�ɂ��A����ɑ����̃R���s���[�e�B���O ���\�[�X��g�p�ł���悤�ɂ��āA�p�t�H�[�}���X����サ�܂��B�ʏ�A�N���X�^�[ �R�l�N�^�́A�����\�v�Z�N���X�^�[�̃x���_�[�ɂ���ĊJ������܂��B</span><span class="sxs-lookup"><span data-stu-id="28d65-p101">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server. For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md). This offloading can improve performance by enabling more computing resources to be used. A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="28d65-109">�N���X�^�[ �R�l�N�^</span><span class="sxs-lookup"><span data-stu-id="28d65-109">Cluster Connectors</span></span>

<span data-ttu-id="28d65-p102">クラスター コネクタは定義済みのエントリ ポイントを提供する DLL です。Excel では、このエントリ ポイントを使用して、クラスター セーフなユーザー定義関数の呼び出しを調整します。これは Excel と高性能計算クラスター間のインターフェイスとして、セッションを管理したり、関数呼び出しを実行 (完全修飾の関数名と呼び出しの実引数を渡すことによる) したり、コールバック メカニズムを使用して Excel に呼び出しの結果を返すために使用します。</span><span class="sxs-lookup"><span data-stu-id="28d65-p102">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls. It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="28d65-112">�N���X�^�[ �R�l�N�^��쐬����ɂ́ADLL ��쐬���āA�u[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)�v�ɋL�ڂ���Ă���G���g�� �|�C���g����J���܂��B</span><span class="sxs-lookup"><span data-stu-id="28d65-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="28d65-113">�N���X�^�[ �R�l�N�^�̃C���X�g�[��</span><span class="sxs-lookup"><span data-stu-id="28d65-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="28d65-p103">�N���X�^�[ �R�l�N�^�� Excel �Ŏg�p�\�ɂ���ɂ́A�R�l�N�^�̃Z�b�g�A�b�v �R�[�h�ŁAExcel ���C���X�g�[������Ă���R���s���[�^�[�ɃR�l�N�^�� DLL ��C���X�g�[������K�v������܂��B����ɁA�R�l�N�^�̃Z�b�g�A�b�v �R�[�h�́A�R�l�N�^�̃G���g������̃��W�X�g�� �L�[�̉��ɒǉ�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="28d65-p103">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed. In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="28d65-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span><span class="sxs-lookup"><span data-stu-id="28d65-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="28d65-117">���̃N���X�^�[ �R�l�N�^�̃L�[�ɁA���̕������w�肷��m�[�h��ǉ����܂��B</span><span class="sxs-lookup"><span data-stu-id="28d65-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="28d65-118">`Name`? Excel ��̃N���X�^�[ �R�l�N�^�̈ꗗ�ɕ\������閼�O�B</span><span class="sxs-lookup"><span data-stu-id="28d65-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="28d65-119">`Filename`? DLL �̊��S�p�X�B</span><span class="sxs-lookup"><span data-stu-id="28d65-119">`Filename`—the full path for the DLL.</span></span>
    

