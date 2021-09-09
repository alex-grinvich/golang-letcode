//https://leetcode.com/explore/learn/card/trie/148/practical-application-i/1053/
package main

import (
	"fmt"
	"strings"
)

type Trie struct {
	isWord bool
	children [26]*Trie
}


/** Initialize your data structure here. */
func Constructor() Trie {
	return Trie{}
}

func (this *Trie) put(word string)  {
	//this.links = append(this.links,Trie{})
}

/** Inserts a word into the trie. */
func (this *Trie) Insert(word string)  {
	cur := this
	for i,c := range word{
		n := c-'a'

		if cur.children[n] == nil {
			cur.children[n] = &Trie{}
		}
		cur = cur.children[n]


		if i == len(word) - 1 {
			cur.isWord = true
		}
	}
}


/** Returns if the word is in the trie. */
func (this *Trie) Search(word string) bool {
	cur := this
	for _,c := range word{
		n := c - 'a'
		if cur.children[n] == nil {
			return false
		}
		cur = cur.children[n]
	}
	return cur.isWord
}


/** Returns if there is any word in the trie that starts with the given prefix. */
func (this *Trie) StartsWith(prefix string) bool {
	cur := this
	for _,c := range prefix{
		n := c - 'a'
		if cur.children[n] == nil {
			return false
		}
		cur = cur.children[n]
	}
	return true
}


func (this *Trie) findPosfix(word string) bool {
	for _,c:= range word{
		q := 'a' - c
		if this.children[q] == nil{
			return false
		}
	}
	return true
}

func trimSuffix (s int,word string) string {
	if s == len(word) {
		return word[:1]
	}
	return word[:s]
}

func (this *Trie) findPrefix(word string) int {
	cur := this
	lastLen := 0
	for i,s:= range word {
		c := s - 'a'
		if cur.children[c] != nil {
			cur = cur.children[c]
			if cur.isWord == true {
				lastLen = i+1
				break
			}
		}else{
			return lastLen
		}
	}

	return lastLen

}

func replaceWords(dictionary []string, sentence string) string {
	this := Constructor()
	t:= strings.Fields(sentence)

	for i := 0; i < len(dictionary); i++ {
		this.Insert(dictionary[i])
	}
	for i,v:= range t{
		word := v
		st := this.findPrefix(word)
		if st != 0 {
			word = trimSuffix(st,word)
		}

		t[i] = word
	}

	return strings.Join(t, " ")
}


type WordDictionary struct {
	children [26]*WordDictionary
	isWord bool
}


/** Initialize your data structure here. */
func Constructor() WordDictionary {
	return WordDictionary{}
}


func (this *WordDictionary) AddWord(word string)  {
	cur := this
	for i,s := range word {
		 c := s - 'a'
		if cur.children[c] == nil {
			cur.children[c] = &WordDictionary{}
		}
		cur := cur.children[c]
		if i == len(word) - 1 {
			cur.isWord = true
		}
	}
}


func (this *WordDictionary) Search(word string) bool {
	status := true
	cur := this
	x
	for i,s := range word{
		if s == '.' {

		}else{

		}
	}
	return status
}
