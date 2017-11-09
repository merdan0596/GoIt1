package com.company;
import static java.lang.Math.*;
import java.io.*;
import java.util.*;
public class  Main {

    public static void main(String args[]){

    }
    int getNumberOfSteps(double begin, double end, double step) {
        double numberOfSteps = (end - begin) / step + 1;
        return (int)numberOfSteps;
    }
    void fillX(double[] x, double begin, double end, double step) {
        int i = 0;
        double dx = begin;
        int len = getNumberOfSteps(begin, end, step);
        for(; i < len; i++, dx = begin + i * step) {
            x[i] = dx;
        }
    }
    void fillY(double[] y, double begin, double end, double step, double eps) {
        int i = 0;
        double dx = begin;
