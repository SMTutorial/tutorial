<script setup>
import { ref, onMounted } from 'vue';
import NestedCard from '../../../components/Cards/ListCard/NestedCard.vue';
import { useTutorialEntryPoint } from "../../../stores/tutorialsEntryPointStore.js";
const tutorialEntryPointStore = useTutorialEntryPoint();

const setTutorialBesics = (tute) => {
    tutorialEntryPointStore.setTutorialData('dart', tute);
}

const setTutorialConditionsAndLoop = (tute) => {
    tutorialEntryPointStore.setTutorialData('dart', tute);
}

const setTutorialFunction = (tute) => {
    tutorialEntryPointStore.setTutorialData('dart', tute);
}

</script>

<template>
    <NestedCard buttonName="Dart Tutorial" backGround="var(--gradient-header)">
        
<!-- =========================================[ DART BASIC ]========================================= -->
        <NestedCard buttonName="Dart Basics" backGround="var(--gradient-one)">
            <button @click="setTutorialBesics('1d1')">Dart Besic</button>

            <NestedCard buttonName="Variables">
                <ol>
                    <li @click="setTutorialBesics('2d1')">Syntax</li>
                    <li @click="setTutorialBesics('2d1_1')">Constant</li>
                    <li @click="setTutorialBesics('2d1_2')">Naming Convention</li>
                </ol>
            </NestedCard>

            <NestedCard buttonName="Data Types">
                <ol>
                    <li @click="setTutorialBesics('3d1')">Types</li>
                    <li @click="setTutorialBesics('3d1_1')">Numbers</li>
                    <li @click="setTutorialBesics('3d1_2')">String</li>
                    <li @click="setTutorialBesics('3d1_3')">Boolean</li>
                    <li @click="setTutorialBesics('3d1_4')">List</li>
                    <li @click="setTutorialBesics('3d1_5')">Sets</li>
                    <li @click="setTutorialBesics('3d1_6')">Maps</li>
                    <li @click="setTutorialBesics('3d1_7')">Runes</li>
                    <li @click="setTutorialBesics('3d1_8')">Statically Typed</li>
                    <li @click="setTutorialBesics('3d1_9')">Dynamically Typed</li>
                </ol>
            </NestedCard>
            <button @click="setTutorialBesics('4d1')">Comments</button>
            <button @click="setTutorialBesics('5d1')">Operators</button>
            <button @click="setTutorialBesics('6d1')">Input</button>
            <!-- <button @click="setTutorialBesics('7d1')">String</button> -->

            <NestedCard buttonName="String">
                <ol>
                    <li @click="setTutorialBesics('7d1')">String</li>
                    <li @click="setTutorialBesics('7d1_1')">String Concatenation</li>
                    <li @click="setTutorialBesics('7d1_2')">String Properties</li>
                    <li @click="setTutorialBesics('7d1_3')">Methods Of String</li>
                </ol>
            </NestedCard>
        </NestedCard>


<!-- =====================================[ Conditions and Loops ]===================================== -->
        <NestedCard buttonName="Dart Conditions and Loops" backGround="var(--gradient-one)">
            <!-- <button @click="setTutorialConditionsAndLoop('1d2')">Conditions</button> -->
            <NestedCard buttonName="Conditions">
                <ol>
                    <li @click="setTutorialBesics('1d2')">If Condition</li>
                    <li @click="setTutorialBesics('1d2_1')">If-Else condition</li>
                    <li @click="setTutorialBesics('1d2_2')">If-Else-If condition</li>
                    <li @click="setTutorialBesics('1d2_3')">Switch-Case</li>
                </ol>
            </NestedCard>
            <button @click="setTutorialConditionsAndLoop('2d2')">Assert</button>
            <button @click="setTutorialConditionsAndLoop('3d2')">Tarnery Operator</button>
            <NestedCard buttonName="Dart Loops">
                <ol>
                    <li @click="setTutorialBesics('4d2')">Loops Types</li>
                    <li @click="setTutorialBesics('4d2_1')">For Loop</li>
                    <li @click="setTutorialBesics('4d2_2')">For Each Loop</li>
                    <li @click="setTutorialBesics('4d2_3')">For In Loop in Dart</li>
                    <li @click="setTutorialBesics('4d2_4')">Find Key & Value</li>
                    <li @click="setTutorialBesics('4d2_5')">While Loop</li>
                    <li @click="setTutorialBesics('4d2_6')">Do While Loop</li>
                </ol>
            </NestedCard>
            <button @click="setTutorialConditionsAndLoop('5d2')">Break and Continue</button>
            <button @click="setTutorialConditionsAndLoop('6d2')">Try and Catch</button>
        </NestedCard>

<!-- =====================================[ FUNCTIONS ]===================================== -->
        <NestedCard buttonName="Dart Functions" backGround="var(--gradient-one)">
            <button @click="setTutorialFunction('1d3')">Function Overview</button>
            <button @click="setTutorialFunction('2d3')">Funticions Type</button>
            
            <NestedCard buttonName="Functions Parameter">
                <ol>
                    <li @click="setTutorialBesics('3d3')">Functions Parameter</li>
                    <li @click="setTutorialBesics('3d3_1')">Positional Parameter</li>
                    <li @click="setTutorialBesics('3d3_2')">Named Parameter</li>
                </ol>
            </NestedCard>
            <button @click="setTutorialFunction('4d3')">Anonymous Function</button>
            <button @click="setTutorialFunction('5d3')">ArrowFunction</button>
            <button @click="setTutorialFunction('6d3')">Scope</button>
            <button @click="setTutorialFunction('7d3')">Math</button>
        </NestedCard>


    </NestedCard>
</template>

<style scoped>
button{
    width: 100%;
    min-height: 3.5rem;
    border: 1px solid gray;
    box-sizing: border-box;
    border-radius: 0.5rem;
    text-align: left;
    padding: 0.5rem;
}
ol{
    list-style-type: none;
    counter-reset: list-counter;
}
ol li{
    background-color: #fcebff;
    min-height: 3rem;
    padding: 0.5rem;
    cursor: pointer;
    font-weight: bold;
    font-size: 1.4rem;
    counter-increment: list-counter;
    list-style-type: none;
}
ol li:nth-child(even){
    background-color: #ffdddd;
}
</style>
